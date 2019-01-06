# turbo-snail
Qualifying Quiz
=============== 



Question 01
-----------  
This test is meant to test your knowledge of C programming and some basic computer science-related skills you will need to do well in this class. The outcome of the test is for your use only; it will not affect whether you can register for the class, and it will not apply to your grade if you do register. As such, we recommend that you do not research the answers on the Internet, but answer the questions to your best recollection.

Consider the following variable declaration for bar in the function foo

```
void foo() {
  char bar[128];
  ...
}
```

Which of the following are true?
- [x] Holds 128 elements
- [ ] bar[1] contains the first element
- [ ] All elements are initialized to 0



Question 02
-----------  
Consider the following code fragment: sizeof(int*) == sizeof(int). Which one of the following is true about it?

- [x] This fragment's result depends on the compiler and architecture
- [ ] This fragment will always crash
- [ ] This fragment always evaluates to 0 (assuming it doesn't crash) 
- [ ] This fragment will not compile 
- [ ] This fragment always evaluates to 1 (assuming it doesn't crash)



Question 03  
-----------  
Suppose you are compiling for a 32-bit platform and sizeof(int) == 4. Which one of the following is equivalent to c[b] if c is of type int* and b is of type int?

- [ ] c[b][0]
- [ ] *c+b
- [ ] -1 * b[c]
- [ ] none of the above
- [x] *(c+b)



Question 04
-----------  
Consider the following program.

```



#include <string.h>

int foo(void) {
  char bar[128];
  char *baz = &bar[0];
  baz[127] = 0;
  return strlen(baz);
}```

- [x] returns 127
- [ ] returns 128
- [x] returns 0
- [ ] crash
- [x] returns -1



Question 05
-----------  
Consider the following code fragment.  

```
char blah[] = "fizzbuzz";
printf("%s\n", blah+4);
```

What happens if we try to compile and run this code?
- [ ] The program is illegal C and may not compile
- [ ] The program outputs "fizz"
- [x] The program outputs "buzz"
- [ ] The program outputs a blank line depending on the size of pointers



Question 06
-----------  
Which of the following are true of memory returned via the malloc function? Check all that apply.  

- [ ] It is automatically released by the operating system when the pointer to which the memory is assigned goes out of scope

- [x] It must be manually released by the programmer
- [ ] The memory is zero-initialized
- [ ] It is write-only



Question 07
-----------  
Consider the following code  

```
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
  unsigned int i;
  unsigned int k = atoi(argv[1]);
  char *buf = malloc(k); /* 1 */
  if(buf == 0) {
    return -1;
  }

  for(i = 0; i < k; i++) {
    buf[i] = argv[2][i]; /* 2 */
  }

  printf("%s\n", buf); /* 3 */

  return -1;
}
```

- [ ] This program could crash at position 2
- [ ] This program could crash at 1 and 2
- [ ] This program could crash at position 1
- [x] This program could crash at 2 and 3
- [ ] This program could crash at position 3
- [ ] This program could crash at all 3 positions



Question 08
-----------  
Which of the following are true statements about the program stack?

- [x] The stack is managed by code emitted by the compiler
- [ ] It is used to store global variables while executing a function
- [x] It is used to store local variables while executing a function
- [ ] It is used as the source of memory returned by malloc()



Question 09
-----------  
Which of the following are true of the X86 call instruction?  

- [x] Its target address may be specified in a general-purpose register
- [x] Pushes the instruction pointer value onto the stack
- [ ] Pushes flag registers onto the stack
- [x] Branches to a specified address 



Question 10
-----------  
Consider the following program

```
#include <stdlib.h>
#include <stdio.h>
#include <string.h>

int main(int argc, char *argv[]) {
  int **blah2 = malloc(sizeof(int*)*N);
  int *special = NULL;
  int i, j;

  for(i = 0; i < N; i++) {
    int *tmp = (int *)malloc(sizeof(int)*M);
    memset((void *)tmp, 0, sizeof(int)*M);
    if(i > N) {
      special = &tmp[3];
    }
    blah2[i] = tmp;
  }

  if(special != NULL) {
    *special = 7;
  }

  for(i = 0; i < N; i++) {
    for(j = 0; j < M; j++) {
      printf("%d ", blah2[i][j]);
    }
    printf("\n");
  }

  return 0;
}
```

Assuming we #define N and M to be positive integers, and the calls to malloc() succeed (the arguments do not overflow, and do not return NULL), then which of the following is true?

- [ ] This is not a valid C program
- [ ] This program outputs a matrix with at least one element being 7
- [ ] This program outputs a random NxM matrix
- [x] This program could crash at 2 and 3
- [ ] This program crashes



Question 11
-----------
What is TCP?

- [x] It is a protocol that supports reliable data transfer on the Internet
- [ ] It is connectionless
- [ ] It ensures data confidentiality
- [ ] It is a protocol often implemented on top of HTTP



Question 12
-----------
What is PHP? Pick one.

- [ ] The acronym for a coding standard
- [ ] A network protocol
- [ ] A programming language often used to implement network switches
- [x] A programming language often used to implement web sites



Question 13
-----------
Which of the following statements about HTML are true?

- [ ] HTML is a kind of URL
- [x] HTML is a text-based format (as opposed to a binary format)
- [x] Web browsers render HTML content served by web sites
- [x] HTML documents have tags that identify different sorts of data



Question 14
-----------
What is gcc?

- [ ] An interpreter
- [ ] All of the above
- [x] A compiler
- [ ] A virtual machine



Question 15
-----------
The shell command cd; ls *.xml

- [ ] Will list all of the files listed in the given XML file
- [ ] Will list all files ending in the xml suffix in the previous working directory
- [x] Will list all files ending in the xml suffix in user's home directory
- [ ] Will list the file *.xml in the current directory

