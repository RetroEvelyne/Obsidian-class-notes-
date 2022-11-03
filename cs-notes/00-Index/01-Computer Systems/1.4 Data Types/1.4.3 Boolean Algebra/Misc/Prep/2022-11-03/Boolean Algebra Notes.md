# Logic Gates
- Processor uses _Binary_ values (__0__ or __1__)
- It is made from _electronic circuits_ which enables us to connect inputs together to create outputs
- These circuits are called _Logic Gates_
- They are:
	- __AND__
		| A   | B   | Q   |
		| --- | --- | --- |
		| __0__   | __0__   | __0__   |
		| __0__   | _1_   | __0__   |
		| _1_   | __0__   | __0__   |
		| _1_   | _1_   | _1_   |
	- __OR__
		| A   | B   | Q   |
		| --- | --- | --- |
		| __0__   | __0__   | __0__   |
		| __0__   | _1_   | _1_   |
		| _1_   | __0__   | _1_   |
		| _1_   | _1_   | _1_   |
	- __NOT__
		| A   | Q   |
		| --- | --- |
		| __0__   | _1_   |
		| _1_   | __0__   | 
	- __XOR__
		| A   | B   | Q   |
		| --- | --- | --- |
		| __0__   | __0__   | __0__   |
		| __0__   | _1_   | _1_   |
		| _1_   | __0__   | _1_   |
		| _1_   | _1_   | __0__   |
	- __NAND__
		| A   | B   | Q   |
		| --- | --- | --- |
		| __0__   | __0__   | _1_   |
		| __0__   | _1_   | _1_   |
		| _1_   | __0__   | _1_   |
		| _1_   | _1_   | __0__   |
	- __NOR__
		| A   | B   | Q   |
		| --- | --- | --- |
		| __0__   | __0__   | _1_   |
		| __0__   | _1_   | __0__   |
		| _1_   | __0__   | __0__   |
		| _1_   | _1_   | __0__   | 

_Logical conditions_: The inputs to the logic operators that affect the output.

# Simplifying Boolean Expressions

## Generic Rules
- AND Rules
	- Because both terms have to be __True__ for the result to be __True__, we can form some generic rules to help simplify operations.
	| #   | Rule       | Explanation                  |
	| --- | ---------- | ---------------------------- |
	| 1   | _X_ __∧__ _0_ __=__ _0_  | _X_ __AND__ _0_ is the same as _0_     |
	| 2   | _X_ __∧__ _1_ __=__ _X_  | _X_ __AND__ _1_ is the same as _X_     |
	| 3   | _X_ __∧__ _X_ __=__ _X_  | _X_ __AND__ _X_ is the same as _X_     |
	| 4   | _X_ __∧ ¬__ _X_ __=__ _0_ | _X_ __AND NOT__ _X_ is the same as _0_ |
- OR Rules
	- Because only one term has to be __True__ for the result to be __True__, we can form some generic rules for these as well.
	| #   | Rule        | Explanation                 |
	| --- | ----------- | --------------------------- |
	| 5   | _X_ __∨__ _0_ __=__ _X_   | _X_ __OR__ _0_ is the same as _X_     |
	| 6   | _X_ __∨__ _1_ __=__ _1_   | _X_ __OR__ _1_ is the same as _1_     |
	| 7   | _X_ __∨__ _X_ __=__ _X_   | _X_ __OR__ _X_ is the same as _X_     |
	| 8   | _X_ __∨ ¬__ _X_ __=__ _1_ | _X_ __OR NOT__ _X_ is the same as _1_ | 
- De Morgan's Law
	- Either logical function __AND__ or __OR__ may be replaced by the other given certain changes to the expression. This means that statements can be simplified so they only use __NAND__ or __NOR__ gates.
	- __¬__(_A_ __∧__ _B_) = __¬__ _A_ __∨__ __¬__ _B_  <=> __NOT__(_A_ __AND__ _B_) is the same as (__NOT__ _A_) __OR__ (__NOT__ _B_)
	- __¬__(_A_ __∨__ _B_) = __¬__ _A_ __∧__ __¬__ _B_  <=> __NOT__(_A_ __OR__ _B_) is the same as (__NOT__ _A_) __AND__ (__NOT__ _B_)
- _Double Negation_ - Two __NOT__'s cancel out
- _Association_ - You can remove brackets and regroup variables
- _Commutation_ - Order of application of two seperate terms is not important

# Other Stuff
- __XOR__ can be used to check if two values _are the same_
- 