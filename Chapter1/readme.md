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
