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

# 1.3 The for statement

You can define a for statement like example blow:

```c
 for (expression 1; expression 2; expression 3) {
  // code block to be executed
}
```

# 1.4 Symbolic Constants

When you have a constant variable that will never changes you can use **`#define name value`** its so easy to declare and you just do this:

```c

#define LOWER 0
#define UPPER 300
#define STEP 20

```

Its not necessary to use Uppercase letter but its better that you write constant variable names with Uppercase letters.

# 1.5 Character Input and Output 

The C Lang read text streams like a bunch of characters that are seperate from each other, Its means that When we read a text stream in C we dont read hole stream or saving the hole texts into a list,
We read text stream character by character. To doing this we will use standard libs that are maden for this.

The standard library provides several functions for reading or writing `one character` at time, of which `puchar` and `getchar` are simplest.

Each time we called `getchar` reads the *next input character* from text stream and returns its value. 

```c

c = getchat();

```

The function `putchar` prints a character each times its called.

```c

putchar(c);

```


# 1.6 Arrays

The Arrays in C are like trains. The are wagons that are conected each others and All of them have a one type (integer, character, double, ...). The Wagons capacity depends on the Arrays type.

Lets write a program that counts the number of occurences of each digits, of white space character, and of all other characters.


```c

#include <stdio.h>

int main(){

    int c, nwhite, nother;
    int ndigit[10];

    nwhite = nother = 0;
    for (int i = 0; i < 10; i++)
        ndigit[i] = 0;

    while ((c = getchar()) != 'q')
        if ( c >= '0' && c <= '9')
            ndigit[c-'0']++;
        else if ( c == ' ' || c == '\n' || c == '\t')
            nwhite++;
        else 
            nother++;

    printf("digits =");
    for (int i = 0; i < 10; i++)
        printf(" %d", ndigit[i]);
    printf(", white space = %d, other = %d\n", nwhite , nother);

    return 0;

}
```


