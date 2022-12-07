## Anatomy of a class
- [[constructors]]
	- no return type
	- define `public <class name>`
	- Can be overloaded with methods for default value or passed in value
	- [[instance variables]] can be defined for class, and accesible by objects of that class type
- [[accessor methods]]
	- methods defined for class to return instance variables
	- `public <return type> <method name>`
	- `class.getInstanceVariable`

## Example bank account
- can model customer account as an object
```java
public class BankAccount {
	public BankAccount()
	{
		String accountNumber;
		String pin;
		double balance;
		String address;
		String accountOpenDate;
	} 
	public double checkBalance
	{
		return BankAccount.balance;
	}
	
	public void withdraw(double amount)
	{
		BankAccount.balance = BankAccount.balance - amount;
		return amount
	}
	
	public void deposit(double amount)
	{
		BankAccount.Balance = BankAccount.balance + amount;
		System.out.println("New balance: " + BankAccount.checkBalance());
	}
	
	public void transferAccount(String transferAccount, double transferAmunt)
	{
		transferAccount.deposit(BankAccount.withdraw(transferAmount));
	}

}
```

- Review: **Static methods vs instance methods for operations on same instance type**\
### Accessor methods
- can create both [[getters]] and [[setters]]
- 