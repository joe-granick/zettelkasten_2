## Basic concepts
-  method's **signature** specifies everything you need to include in a function call
	- `public static double sqrt(double c, double eps)`
- keeping **scope** local important to **modularity**
	- **functions** help contain scope, with variables **local** to methods unusable outside of it
- **functions** let you alter the **flow-of-control**
- **pass by value** java initializes parameter variable by evaluating the provided argument and assigning it to the variable
- **compile errors**
- Don't want to change function arguments in code

## Case Study: Digital Audio
- **Sound** is perception of the vibration of molecules
- Musical **tone** is a steady periodic sound
- a **pure** tone is a sinusoidal wave form
- Frequency of **sine wave** makes different notes
- **Concert A** defined at `440 hz`
	- 12 notes
	- logarithmic scale
| pitch | $i$ | $\text{frequency}(440*2^{i/12})$ |
| ----- | --- | -------------------------------- |
| A     | 0   | 440.00                           |
| A#/B  | 1   | 466.16                           |
| B     | 2   | 493.88                           |
| C     | 3   | 523.25                           |
| C#/D  | 4   | 554.37                           |
| D     | 5   | 587.33                           |
| D#/E  | 6   | 622.25                           |
| E     | 7   | 659.26                           |
| F     | 8   | 698.46                           |
| F#/G  | 9   | 739.99                           |
| G     | 10  | 783.99                           |
| G#/A  | 11  | 830.61                           |
| A     | 12  | 880.00                           |

- With **digital audio** we can represent a wave by sampling at regular intervals and saving the values in an array

### Guassian Distribution

### Modular Programming and Libraries
