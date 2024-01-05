## FINAL PROJECT: EMUCORE

This codebase consists of SimpleLogic library functions in addition to an Arithmetic Logic Unit (ALU) simulation written in C. The ALU simulation does a variety of arithmetic and logical operations on binary data provided by the SimpleLogic library.

simplelogic/simplelogic.h: Header file incorporates bit manipulation and arithmetic/logic operations definitions. The main.c file provides functions and routines for arithmetic operations such as addition, subtraction, multiplication, and division with binary data.

**Functions**
BITINT2BIT(): Converts a long long integer to a 16-bit binary representation.

DUPEBIT(): Copies the contents of one binary array to another.

invert(): Inverts a binary array by flipping its bits.

adder16(): Performs 16-bit binary addition.

sub16(): Performs 16-bit binary subtraction.

div16(): Performs 16-bit binary division.

multi16(): Performs 16-bit binary multiplication.

ALU(): Controls the Arithmetic Logic Unit based on the operation code (O).

Counter Functions: Includes functions to manage and increment counters.

Counter Functions: This group of tasks includes functions for managing and incrementing counters.

Main Function: Executes the ALU simulation using instruction set data, manipulating memory, instructions, registers, and the bus.

Set of Instructions
The simulation follows to a predefined instruction set, which includes a variety of operations and micro-instructions. Each instruction is encoded with a unique binary code. Some instructions execute arithmetic/logic operations, while others change registers or memory.

This is from the pervious lab. "Create a new directory, call it `simplelogic`. 
* Create two source files, `simplelogic.h`, and `simplelogic.c`. In `simplelogic.h`, you need to place the `bit` type definition and all the function prototypes you've previously created for this lab. Be sure to use header guards: [link](https://en.wikipedia.org/wiki/Include_guard).
* In `simplelogic.c`, place the implementations of all your functions. It also needs to `#include` your new header file. 
* Compile the `simplelogic.c` (and potentially also `gnuplot_i.c`) to generate a single `.o` object file, using the `-fPIC` flag to indicate that we are generating "position independent code", i.e. a piece of machine code that will later be moved as part of a larger executable:"

you can get a clear picture from this and the project how it works. 


**Format of Instructions**

The instruction format is divided into two parts: The first (12-bit) component is the operation code (Opcode). 

Second (5-bit) segment: Instruction-specific data or memory addresses 

Examples of Instructions 

-AIN: Load data to register A from memory location. 

-BIN: Load data into register B from memory address. 

-LDIA: Load a value into register A immediately. 

-ADD: Add the values in registers A and B. 

-MULT: Multiply the values in registers A and B. 

-JMP: Navigate to a certain counter value. 

**Micro-Instructions** 

Micro-instructions are little actions that are performed within the ALU, each with a specific purpose such as reading from or writing to registers, memory, or performing other control operations. 

Here is the code to place in the Shell to complie and run it many times: 

from the lab 6 README "Implement function `adder32()` which takes as input two 32-bit inputs `A` and `B`, and models a ripple-carry adder to produce 32-bit output `S`. Since these are all arrays, use the following function prototype:"
```c
"void adder32(bit A[], bit B[], bit S[]);"

Here we used 32 but in the project we used 16 bits. 
