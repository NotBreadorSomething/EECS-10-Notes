### Intro
10% of code is for automation
90% is to control hardware

C++ is just C with more stuff : can be added to resume

Embedded Hardware: Using C or another program to control hardware. C program is the glue that holds the hardware together.

` C = 5 ` Software stores 5 somewhere in hardware memory. We do not know this location so we assign it as C. 

Processors are a series of on and off switches, like closing the valves in a pipe. 
### Assembly and a better language
**Machine Language:** Code in 0 and 1's. Binary.

Instead of using binary, you could use symbols. This is assembly language.
```
add A,B --> 010 010 011
            add  2   3
```
This code must be translated by a complier back into binary.
The issue with assembly language, is it is hardware dependent. 
Example:

| Intel Processor | Add Ax, Bx       |
| --------------- | ---------------- |
| Motorola        | Add D$_1$, D$_2$ |

So the issue is why can't we create a universal language. Solution? A High Level Language, such as C / C++. As long as your computer has a translator (Complier) it will run the code.

A downside of HLL is the lack of control of hardware. Using assembly you can control where data is stored, while in HLL you cannot. 

Point is, that hardware will ALWAYS need 0's and 1's, regardless of language you use. 

### What is on? What is off?
Everything in computers is low and high voltage (So basically binary).

We have the following voltages:

```
2.3, 4.5, 0.5, 0.25
```

But reading that is hard so we declare a threshold, say 3 volts. Everything above it is on, everything below it is off. As a result our voltages can just be written as:

```
2.3, 4.5, 0.5, 0.25 --> 0100
```

However this is more like a range, as something between say, 1 and 2 volts can be ambiguous. 

Transistors are switches that are made with silicon. Before they used relays with actual wires. 

### Describing Storage
But how do we describe the size of data. 

| Name     | Symbol | Value           |
| -------- | ------ | --------------- |
| Bit      |        | One bit of data |
| Byte     |        | 8 bits          |
| Kilobyte | KB     | 1024 bytes      |
| Megabyte | MG     | 1024 KB         |
| Gigabyte | GB     | 1024 GB         |
Computers uses bytes in order to be able to tell when a new digit starts and ends.
So if we have a list of binary, `0100101011100110` we would divide it in eights, `01001010 11100110`.
### Converting Decimal to Binary
Divide decimal you need to divide by 2, and continue until you have no remainder.

| Binary             | 1     | 1     | 0     | 1     | 0     | 11010 |
| ------------------ | ----- | ----- | ----- | ----- | ----- | ----- |
| Decimal Equivilant | $2^4$ | $2^3$ | $2^2$ | $2^1$ | $2^0$ | 26    |
| Transistor is      | On    | On    | Off   | On    | Off   |       |

### Non-number Values
In cases where we want to say show a character like \*, we would need to something like ASCII.
ASCII is just a table of bits that binary references.

### Operations
But what about when you want to do operations like addition?

Every system has it's own symbol reserved for it's operations. There is a code unique for every processor.

### Summary
The course a C program. The language is HLL. It must all be converted back to binary via a complier so that the computer can use it. 