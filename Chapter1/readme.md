# 1.1 Getting Started 

Crate a file called hello.c and write this code in the file:

```c

#include <stdio.h>

int main(){
    
    printf("hello, world\n");

}
```

This our first program in C, We can compile it by GCC:

```bash

gcc hello.c -o helloWorld
```

The '-o helloWorld' argument means the output file name is 'helloWorld'

### Exercise 1-2

When we add \c escape sequence to our string C gives Error:

```
exercise1-2.c: In function ‘main’:
exercise1-2.c:5:26: warning: unknown escape sequence: '\c'
    5 |   printf("hello, world\c");
      |
```

The reason is that C does not have any \c escape sequence.

# 1.2 Variable and Arithmetic Expressions

The program that written in this part is a code that convert *Fahrenheit* to *Celsius* :

```c
#include <stdio.h>

int main(){

  float fahr, celsius;
  float lower, upper, step;

  lower = 0;
  upper = 300;
  step = 20;

  fahr = lower;

  while (fahr <= upper){

    celsius = (5.0/9.0) * (fahr - 32.0);
    printf("%3.0f \t %6.1f\n", fahr, celsius);
    fahr = fahr + step;

  }

  return 0;

}
```

There is some inresting feature in **C** that We can costumize our integer and float numbers in output:

```c

printf("%3.0f \t %6.1f\n", fahr, celsius);

```

In the "%3.0f" and "%6.1" numbers before the dot means the how long digit can have ours number and the number after the dot means that how many decimal digit output can have.

> NOTICE: The number before the dot that determines how many digit we can have, Its include minus sign and the dot itself's.
