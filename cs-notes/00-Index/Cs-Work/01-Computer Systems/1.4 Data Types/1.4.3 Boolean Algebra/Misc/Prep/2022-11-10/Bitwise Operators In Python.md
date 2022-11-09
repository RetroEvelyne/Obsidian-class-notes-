We use _operators_ to perform an action on variables and values. In __Python__, operators can perform both _logical_ and _arithmetic_ operations on values which are called _operands_. These are used in conditional and logical statements to test a condition and then perform a routine.

## Types of operators --
Operations are performed at the machine readable bit level, while the result is returned in human readable decimal format.
| Symbol | What It Represents  | Example |
| ------ | ------------------- | ------- |
| &      | Bitwise AND         | x & y   |
| \|     | Bitwise OR          | x \| y  | 
| ~      | Btiwise NOT         | ~x      |
| ^      | Bitwise XOR         | x ^ y   |
| >>     | Bitwise Right Shift | x>>     |
| <<     | Bitwise Left Shift  | x<<     |

### Bitwise AND
The operator symbol for __AND__ is "__&__". The statement is __True__ (_1_) if the value of _x_ and _y_ are _1_. Both values must be equal to 1, if only one variable is 1 the result is __False__ (_1_).

### Bitwise OR
The operator symbol for __OR__ is "__|__". The statement is __True__ (_1_) is either value of _x_ or _y_ are _1_. Both values must be equal to _0_ for the result to be _0_. 

### Bitwise NOT
The operator symbol for __NOT__ is "__~__". This is a negation operator meaning the output is the the opposite value of the input. If _x_ = _1_ then __~__ _x_ = _0_ and vice versa.

### Bitwise XOR
The operator symbol for __XOR__ is "__^__". All values returned will be __False__ (_0_), unless only one value is __True__ (_1_).
e.g. x = 1, y = 0, x ^ y = 1

### Bitwise Shifting
Bitwise shift operators move or shift the position of bits either to the left or to the right. Shifting to the right "__>>__" is the same as dividing a number and shifting to the left "__<<__" is the same as myltiplying a number.
e.g.
	```x = 10
	Bitwise Shift Right
	x >> 1 = 5
	x >> 2 = 2
	Bitwise Shift Left
	x << 1 = 20
	x << 2 = 40 ```

__This all means that we can represent logical circuit diagrams in code.__
