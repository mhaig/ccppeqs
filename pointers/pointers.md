# Pointers

Collection of questions involving pointers and pointer manipulation.

## Question 1

Write code in C which accepts one argument and creates an array of integers, the
length of which is the argument.  Fill the array with random integers and print
the array.

### Extra Credit

Print the array again using a different mechanism to access the elements of the
array.

## Question 2

Finish this code block.

> :bulb: Only the two functions with `@todo` need to be implemented, no other
> code needs to be written or altered.

> :bulb: This can be solved with no additional memory allocations or additional
> memory copies.

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

/** String that will played with in this example. */
char longString[] = "This is a long string that you will have to do stuff to.";

/**
    @brief Returns a pointer to the "second" half of a string.

    For example, with a string of length 20, return a pointer to the contents of
    position 10 to the end.
*/
static char*
getSecondHalf(char* string)
{
    /** @todo Implement this function. */
}

/**
    @brief Returns a pointer to the "first" half of a string.

    For example, with a string of length 20, return a pointer to the contents of
    position 0 to position 9.
*/
static char*
getFirstHalf(char* string)
{
    /** @todo Implement this function. */
}

/** @brief Main program entry point.
    @param[in] argc  Unused
    @param[in] argv  Unused
    @retval 0
        Success.
*/
int
main(int argc, char *argv[])
{

    char* string = malloc(sizeof(longString));

    (void) argc;
    (void) argv;

    memset(string, 0, sizeof(longString));
    memcpy(string, longString, sizeof(longString)-1);

    printf("Entire string: %s\n", string);
    printf("Second half of string: %s\n", getSecondHalf(string));
    printf("First half of string: %s\n", getFirstHalf(string));

    free(string);
    return 0;
}
```
