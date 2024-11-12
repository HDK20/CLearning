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
