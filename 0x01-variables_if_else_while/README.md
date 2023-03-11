# Things to remember
## rand()

* The rand() function is used to generate a sequence of pseudo-random numbers. A pseudo-random number is a number that appears to be random, but is actually determined by a deterministic algorithm. 
* The rand() function generates a sequence of integers between 0 and RAND_MAX, which is a constant defined in the stdlib.h header file.
To use rand() function, you need to call srand() function first, which sets the seed for the random number generator. If you do not set the seed, the generator will produce the same sequence of numbers every time you run the program. You can set the seed by passing an integer value to the srand() function, such as srand(12345);

~~~~
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int random_number;
    
    srand(time(NULL)); // set the seed based on current time
    
    random_number = rand() % 100; // generate a random number between 0 and 99
    
    printf("Random number: %d\n", random_number);
    
    return 0;
}
~~~~
