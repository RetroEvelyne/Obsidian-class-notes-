# Binary Equivalence Tester

Using logic, you are able to build a circuit that tests whether two binary numbers are the same.
This is made by putting a _XOR_ gate and then a _NOT_ gate. This is because the _XOR_ gate will output __True__ only if the inputs are different. To test if they are the same we just reverse the _XOR_ gate's output by using a _NOT_ gate

__The Truth Table And Diagram For An Equivalence Tester:__
	| A   | B   | Output |
	| --- | --- | ------ |
	| 0   | 0   | 1      |
	| 0   | 1   | 0      |
	| 1   | 0   | 0      |
	| 1   | 1   | 1      |
	![[Binary_Equivalence.svg]]


# Binary Half Adder
Processors can only do a very limited amount of operations on binary data, these simply boil down to:
	> Adding
	> Shifting
	> Flipping

A __Binary Half Adder__ adds two single bit binary numbers together. Only 4 calculations are actually possible and they are:
	> __0__ + __0__ = __0__
	> __0__ + _1_ = _1_
	> _1_ + __0__ = _1_
	> _1_ + _1_ = _1_ __0__
	The result from the final calculation is interesting as it cannot be stored with a single bit, therefore we _Carry_ the _1_.

__The Truth Table And Diagram For A Half Adder:__
	| Input 1 | Input 2 | Sum | Carry |
	| ------- | ------- | --- | ----- |
	| 0       | 0       | 0   | 0     |
	| 0       | 1       | 1   | 0     |
	| 1       | 0       | 1   | 0     |
	| 1       | 1       | 0   | 1     | 
	![[Binary_Half_Adder.svg]]


# Binary Full Adder
This is the circuit needed to add bigger numbers than a __Half Adder__. It takes any carried bits into account in the calculation, therefore _three inputs are needed_.

__The Truth Table And Diagram For A Full Adder:__
	| A   | B   | Cin | Cout | S   |
	| --- | --- | --- | ---- | --- |
	| 0   | 0   | 0   | 0    | 0   |
	| 0   | 0   | 1   | 0    | 1   |
	| 0   | 1   | 0   | 0    | 1   |
	| 0   | 1   | 1   | 1    | 0   |
	| 1   | 0   | 0   | 0    | 1   |
	| 1   | 0   | 1   | 1    | 0   |
	| 1   | 1   | 0   | 1    | 0   |
	| 1   | 1   | 1   | 1    | 1   | 
	![[Binary_Full_Adder.svg]]


# Multi Bit Binary Adder
__Full Adders__ can be chained together to add numbers that take up multiple bits.
Think of a __Full Adder__ like one functional block with three inputs and two outputs like this:
	![[One_Bit_Full_Adder.svg]]

You can then chain as many of them together as is needd to add multi bit numbers. The $C_{out}$ from one adder feeds into the $C_{in}$ of the next adder.

__For Example This Is The Diagram For A Four Bit Adder:__
	![[Four_Bit_Full_Adder.svg]]
	Notice that these chains start with a __Half Adder__ because there is no $C_{in}$ for the first operation.


# Sequential Circuits
All circuits so far are _combination circuits_ where the outputs depend entirely on the inputs.
__Flip-flops__ are not _combination circuits_ but they are what is called _sequential circuits_ where the outputs depend not only on the current inputs but also on the sequence of past inputs. A __flip-flop__ allows for a previous output value to be stores and thus acts as a simple memory device. These memory units are _volatile_.

_sequential circuits_ can be _asynchronous_ or _synchronous_. In an _asynchronous circuit_ the inputs will be processed as they arrive, In a _synchronous circuit_ the operations are controlled by a __clock__.


# D-type flip-flop
This __flip-flop__ is a _synchronous sequential circuit_ that can be used to store the value of a single binary digit.

It has _two external inputs:_
	> A data signal ($D$)
	> A clock signal ($Clk$)
And _two external outputs:_
	> Output ($Q$)
	> __NOT__ Output ($\bar{Q}$)
When the clock signal is low (__0__), changes as $D$ make no difference to the outputs. When the clock signal is high (__1__), then the value of $D$ will appear at output $Q$. $\bar{Q}$ is always the inverse of $Q$.

__Truth Table And Diagram:__
	![[D_Flip-Flop.svg]]
