[[EECS 10 Intro#Summary|Recap]] 
### Programming Example

```
// Lab1
#include <stdio.h> // This is a library. 

int main() // This is a function
{
// Every line must end with semicolin to tell compiler that a new line is made
// When declaring a variable you must declare the type; int, str, bool, float

int c = 5;  
int d = 6;
int z = c + d;

return z;

}
```

When you store `int c = 5` the computer stores 5 in binary in some location in memory
The same thing occurs when you store `int d = 6`.
However when you do a process like `int z = d + c`, the computer tells the processor to prepare the adder and takes `c` and `d` from memory and adds them together. The result is then saved in memory as `z`.

Instead of declaring `int z = c + d` we can declare `z` seprately, so like this.
```
// Lab1
#include <stdio.h> // This is a library. 

int main() 
{
int c = 5;// define c as 5
int d = 6;// define d as 6
int z;    // define z as a placeholder variable
z = c + d;// then you can use z, c, and d

}
```
#### Using print
When printing you need to use `printf();`. For example if you want to print the value of `z` you need to tell the computer at was position, with `%d`. So `printf("name is=   %d", z);` while print out `name is=   11`. If we removed name is=, then it would print out `11`.

When printing multiple variables you need to use `%d` for each integer. When using floats we use `%f` and `%c` for characters. 

| Type   | Placeholder |
| ------ | ----------- |
| int    | %d          |
| float  | %f          |
| char   | %c          |
| string | $s          |
So if we wanted to print `c`, `d`, and `z`, we would need to write `printf("%d%d%d", c,d,z);` This will print out `5611`. 

This isn't readable. As a result we might want to add a new line. to do this we need to use `\n`. So instead of `printf("%d%d%d", c,d,z);` we can do something like `printf("c = %d\nd = $d\nz = %d\n",c,d,z);` which will output: 
```
c = 5
d = 6
z = 11

```

| Symbol         | Definition                                 |
| -------------- | ------------------------------------------ |
| \n             | new line                                   |
| \t             | tab                                        |
| //             | comment                                    |
| /*   \*/       | multi line comment                         |
| printf("%d",z) | print function                             |

#### Using Scanf
`scanf` is a function that listens for keyboard inputs. Like print, scanf needs a position and then any variable.
```
. . .

scanf("%d",&a);

. . .
```
Here, the `&` is saying that whatever input `scanf` receive to store it at that address. In this case, store the input at `int a =`. Because of the `%d` it is a assumed that the input will be an integer. 

When we run the code, we will receive a blinking curser that awaits for user input. 

However there is an issue with this. As the user we do not KNOW what to do. So its a good idea to put print instructions before using scanf.

#### Using operations
In C/C++ there are plenty of operations.  Below is a table with the operations in C/C++.

| Symbol | Operation        |
| ------ | ---------------- |
| +      | addition         |
| -      | subtraction      |
| /      | division         |
| *      | multiplication   |
| %      | modular division |
| **     | exponiation      |
The important thing to note is that data type is important. When you divide two integers, you will get an integer. 

What about something like this below? 
```
 A = 4 * 5 + 4 % 3 * 5
```
In this case Exponents take priority, followed by Multiplication, Division, and Mod and finally addition and subtraction are done last. 
If the same rank is in the same line, we go left to right. 
```
A = 4 * 5 + 4 % 3 * 5
A = 20 + 4 % 3 * 5
A = 20 + 1 * 5
A = 20 + 5
A = 25
```
### Formatting variables

When declaring variables, do the best to match the context of the variable. 
You can you A-Z, 0-9 and underscores to name variables. The first letter cannot be a number, but it can be an underscore.

C/C++ is case sensitive.

### How different data types are stored

When you use `int` the computer can use 16 bit to store the variable. So when you store `int c = 5` the computer will store 5 as `0000000000000101`.

When you use float, the computer needs to use floating point calculation. so 5 becomes $0.101 * 2^3$ and the exponent and base must be saved somewhere. 

