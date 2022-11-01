## 1. Gas
### Inputs
- `gallonPrice`
- `gallonPurchased`
- `credit`
### Outputs
- `"Price Paid"`
### Algorithm
```
SET(1) gallonPrice TO READ(2) price 
SET(3) gallonPurchase TO READ(4) gallons (2)
SET(5) credit TO READ(6) creditCard
IF creditCard is True THEN (7)
	DISPLAY(8) COMPUTE(9) gallonPrice*gallonPurchase*1.1
ELSE 
	DISPLAY(8) COMPUTE(9) gallonPrice*gallonPurchase
   
```
### Test Cases
- (price = 4.50, gallons = 16, creditCard = True)
### Min operations
- 9
### Max operations 
- 9
