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

## Tips
* In C programming, the expression n % 10 calculates the remainder when n is divided by 10.

* For example, if n is equal to 25, then n % 10 will evaluate to 5, since 25 divided by 10 leaves a remainder of 5.

* The expression m = n % 10; assigns the result of n % 10 to the variable m. This means that m will now contain the last digit of the number n.
~~~~
#include <stdio.h>

int main() {
    int n = 12345;
    int m = n % 10; // calculate the last digit of n
    
    printf("n = %d\n", n); // output the value of n
    printf("m = %d\n", m); // output the last digit of n
    
    return 0;
}
~~~~

* In this example, we assign the value 12345 to the variable n. We then use the expression n % 10 to calculate the last digit of n, which is 5. We assign this value to the variable m using the statement m = n % 10;. Finally, we use the printf() function to output the values of n and m to the console. The output will be: 
~~~~
n = 12345
m = 5
~~~~
