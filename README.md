# CodeChum_Study_Area_Exercises

LESSON 3 Input/Output

Topic 1 Output Operations

1. Hello World<br>
Write a program that prints the string "Hello, World!" to the console.

#include <stdio.h>

void main() {

    printf("Hello, World!");
}


2. Odd or Even<br>
Write a program that takes an integer as input and prints whether the number is odd or even.

#include <stdio.h>

void main() {

    int n;

    printf("Enter an integer: ");
    scanf("%d", &n);

    if(n%2 == 0) printf("%d is even.", n);
    else printf("%d is odd.", n);
}


3. ASCII Art<br>
Write a program that prints an ASCII art of a chosen character to the console.

#include <stdio.h>

void main() {

    char c; 

    printf("Enter a character: ");
    scanf(" %c", &c);
    printf("ASCII art of %c: ", c);

    printf("\   __%c__\n", c);
    printf("  /     \\\n");
    printf(" |   o   |\n");
    printf("(|  (_)  |)\n");
    printf(" |   |   |\n");
    printf(" |  / \\  |\n");
    printf(" |       |\n");
    printf(" |       |\n");
    printf(" |_______|");
}


4. Multiplication Table<br>
Write a program that takes an integer as input and prints its multiplication table up to 10.

#include <stdio.h>

void main() {

    int n;

    printf("Enter a number: ");
    scanf("%d", &n);

    for(int i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", n, i, n * i);
    }
}


5. Print a Rectangle<br>
Write a program that takes two integers (width and height) as input and prints a rectangle of asterisks (*) with the given dimensions.

#include <stdio.h>

void main() {

    int w, h;

    printf("Enter width: ");
    scanf("%d", &w);
    printf("Enter height: ");
    scanf("%d", &h);

    for(int i = 0; i < h; i++) {
        for(int j = 0; j < w; j++) {
            printf("*");
        }
        printf("\n");
    }
}


6. Leap Year<br>
Write a program that takes a year as input and prints whether it is a leap year or not.

#include <stdio.h>

void main() {

    int year;

    printf("Enter a year: ");
    scanf("%d", &year);

    if(year % 4 == 0) {
        printf("%d is a leap year.", year);
    }
    else {
        printf("%d is not a leap year.", year);
    }
}


7. Fahrenheit to Celsius<br>
Write a program that takes a temperature in Fahrenheit as input and prints its equivalent temperature in Celsius.

#include <stdio.h>

void main() {

    float temp;

    printf("Enter temperature in Fahrenheit: ");
    scanf("%f", &temp);

    temp = ((temp - 32) * 5) / 9;

    printf("Temperature in Celsius: %.2f", temp);
}


8. BMI Calculator<br>
Write a program that takes a person's weight and height as input and prints their BMI (body mass index).

#include <stdio.h>

void main() {

    float w, h, bmi;

    printf("Enter weight in kilograms: ");
    scanf("%f", &w);
    printf("Enter height in meters: ");
    scanf("%f", &h);

    bmi = w / (h * h);

    printf("BMI: %.2f", bmi);
}


9. String Concatenation<br>
Write a program that takes two strings as input and concatenates them together, printing the resulting string to the console.

#include <stdio.h>
#include <string.h>

void main() {

    char f[1000];
    char s[1000];

    printf("Enter the first string: ");
    fgets(f, 1000, stdin);
    f[strlen(f)-1] = '\0';

    printf("Enter the second string: ");
    fgets(s, 1000, stdin);
    s[strlen(s)-1] = '\0';

    printf("Concatenated String: %s", strcat(f, s));
}


10. Diamond Pattern<br>
Write a program that takes an integer as input and prints a diamond pattern of asterisks (*) with the given dimensions.

#include <stdio.h>

void main() {

    int n, i, j;

    printf("Enter an odd integer: ");
    scanf("%d", &n);

        for(i = 1; i <= n/2 + 1; i++) {
            for(j = 1; j <= n/2 + 1 - i; j++) {
                printf(" ");
            }
            for(j = 1; j <= i * 2 - 1; j++) {
                printf("*");
            }
            printf("\n");
        }
        for(i = n/2; i >= 1; i--) {
            for(j = 1; j <= n/2 + 1 - i; j++) {
                printf(" ");
            }
            for(j = 1; j <= i * 2 - 1; j++) {
                printf("*");
            }
            printf("\n");
        }
}

_____________________________________________________________________________________________________________________
Topic 2 Input Operations

1. Currency Converter<br>
Write a program that reads in an amount in USD and converts it to another currency based on the current exchange rate.

#include <stdio.h>

void main() {

    float amount, rate;

    printf("Enter amount in USD: ");
    scanf("%f", &amount);
    printf("Enter exchange rate: ");
    scanf("%f", &rate);

    printf("Result: %.2f", amount * rate);
}

2. ASCII Art<br>
Write a program that reads in a character and prints an ASCII art representation of it. The program should only accept alphanumeric characters (i.e., A-Z, a-z, and 0-9). For each character, the program should print an ASCII art representation in the form of a rectangle, where the width of the rectangle is 5 characters and the height is 7 characters.

#include <stdio.h>

void main() {

    char c;

    printf("Enter a character: ");
    scanf(" %c", &c);

    if((c >= '0' && c <= '9') || (c >= 'A' && c <= 'Z') || (c >= 'a' && c <= 'z')) {
        printf("*****\n");
        printf("*   *\n");
        printf("* %c *\n", c);
        printf("*   *\n");
        printf("*****");
    }
    else {
        printf("Invalid input.");
    }
}

<br><br><br><br>
LESSON 4 Operators
<br><br>
Topic 1 Arithmetic Operators

1. Sum of Two Numbers<br>
Write a program that takes two integers as input and returns their sum.

#include <stdio.h>

void main() {

    int a, b;

    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);

    printf("The sum of %d and %d is %d", a, b, a + b);   
}


2. Difference of Two Numbers<br>
Write a program that takes two integers as input and returns their difference.

#include <stdio.h>

void main() {

    int a, b;

    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);

    printf("The difference of %d and %d is %d", a, b, a - b);   
}


3. Product of Two Numbers<br>
Write a program that takes two integers as input and returns their product.

#include <stdio.h>

void main() {

    int a, b;

    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);

    printf("Product of %d and %d is %d", a, b, a * b);   
}


4. Quotient of Two Numbers<br>
Write a program that takes two integers as input and returns their quotient. If the divisor is zero, return an error message.

#include <stdio.h>

void main() {

    int a, b;

    printf("Enter dividend: ");
    scanf("%d", &a);
    printf("Enter divisor: ");
    scanf("%d", &b);

    if(b == 0) {
        printf("Error: divisor cannot be zero");
    }
    else {
        printf("Quotient = %d", a / b);
    }
}


5. Remainder of Two Numbers<br>
Write a program that takes two integers as input and returns their remainder. If the divisor is zero, return an error message.

#include <stdio.h>

void main() {

    int a, b;

    printf("Enter dividend: ");
    scanf("%d", &a);
    printf("Enter divisor: ");
    scanf("%d", &b);

    if(b == 0) {
        printf("Error: divisor cannot be zero.");
    }
    else {
        printf("Remainder = %d", a % b);
    }
}


6. Absolute Value<br>
Write a program that takes an integer as input and returns its absolute value.

#include <stdio.h>

void main() {

    int a;

    printf("Enter an integer: ");
    scanf("%d", &a);
    
    if(a < 0) {
        a *= -1;
        printf("The absolute value of -%d is %d", a, a);
    }
    else {
        printf("The absolute value of %d is %d", a, a);
    }
}


7. Power of a Number<br>
Write a program that takes two integers as input and returns the first number raised to the power of the second number.

#include <stdio.h>

void main() {

    int a, b, c;

    printf("Enter base number: ");
    scanf("%d", &a);
    printf("Enter exponent number: ");
    scanf("%d", &b);

    c = a;

    for(int i = 0; i < b - 1; i++) {
        a *= c;
    }
    
    printf("Result: %d", a);
}


8. Average of Three Numbers<br>
Write a program that takes three integers as input and returns their average.

#include <stdio.h>

void main() {

    float a, b, c;

    printf("Enter three numbers: ");
    scanf("%f %f %f", &a, &b, & c);

    printf("Average of the three numbers: %.2f", (a + b + c) / 3);
}


9. Increment a Number<br>
Write a program that takes an integer as input and increments it by 1.

#include <stdio.h>

void main() {

    int a;

    printf("Enter an integer: ");
    scanf("%d", &a);

    a++;
    
    printf("Result: %d", a);
}


10. Decrement a Number<br>
Write a program that takes an integer as input and decrements it by 1.

#include <stdio.h>

void main() {

    int a;

    printf("Enter an integer: ");
    scanf("%d", &a);

    a--;
    
    printf("The decremented value is: %d", a);
}

<br><br><br><br>
Topic 2 Assignment Operators

1. Swap Two Numbers<br>
Write a program that swaps the values of two variables using the assignment operator.

#include <stdio.h>

void main() {

    int a, b, c;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);
    
    printf("Before swap a = %d, b = %d\n", a, b);

    c = a;
    a = b;
    b = c;
    
    printf("After swap a = %d, b = %d", a, b);
}


2. Increment and Assign<br>
Write a program that increments a variable by a certain amount using the += operator.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value: ");
    scanf("%d", &a);
    printf("Enter increment value: ");
    scanf("%d", &b);
    
    printf("Before increment a = %d\n", a);

    a += b;
    
    printf("After increment a = %d", a);
}


3. Decrement and Assign<br>
Write a program that decrements a variable by a certain amount using the -= operator.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value: ");
    scanf("%d", &a);
    printf("Enter decrement value: ");
    scanf("%d", &b);
    
    printf("Before decrement a = %d\n", a);

    a -= b;
    
    printf("After decrement a = %d", a);
}


4. Multiply and Assign<br>
Write a program that multiplies a variable by a certain amount using the *= operator.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);
    
    printf("Before multiplication a = %d\n", a);

    a *= b;
    
    printf("After multiplication a = %d", a);
}


5. Divide and Assign<br>
Write a program that divides a variable by a certain amount using the /= operator.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);
    
    printf("Before division a = %d\n", a);

    a /= b;
    
    printf("After division a = %d", a);
}


6. Modulo and Assign<br>
Write a program that finds the remainder of a variable divided by a certain amount using the %= operator.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);
    
    printf("Before modulo a = %d\n", a);

    a %= b;
    
    printf("After modulo a = %d", a);
}


7. Bitwise AND and Assign<br>
Write a program that performs a bitwise AND operation on a variable and a certain number using the &= operator.

#include <stdio.h>

void main() {

    int a, b;

    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);
    
    printf("Before bitwise AND and assign operation, a = %d\n", a);

    a &= b;

    printf("After bitwise AND and assign operation, a = %d\n", a);
}


8. Bitwise OR and Assign<br>
Write a program that performs a bitwise OR operation on a variable and a certain number using the |= operator.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);
    
    printf("Before OR, a = %d\n", a);

    a |= b;
    
    printf("After OR, a = %d", a);
}


9. Bitwise XOR and Assign<br>
Write a program that performs a bitwise XOR operation on a variable and a certain number using the ^= operator.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);

    a ^= b;
    
    printf("Result: %d", a);
}

<br><br><br><br>
Topic 3 Bitwise Operators

1. Bitwise AND<br>
Write a program that takes two integers as input and performs a bitwise AND operation on them.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);
    
    printf("The result of the bitwise AND operation is: %d", a & b);
}


2. Bitwise OR<br>
Write a program that takes two integers as input and performs a bitwise OR operation on them.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);
    
    printf("Bitwise OR result: %d", a | b);
}


3. Bitwise NOT<br>
Write a program that takes an integer as input and performs a bitwise NOT operation on it.

#include <stdio.h>

void main() {

    int a;
    
    printf("Enter a number: ");
    scanf("%d", &a);
    
    printf("Bitwise NOT of %d is %d", a, ~a);
}


4. Left Shift<br>
Write a program that takes two integers as input and performs a left shift operation on the first integer by the number of bits specified by the second integer.

#include <stdio.h>

void main() {
    
    int a, b;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);

    printf("%d", a << b);
}


5. Right Shift<br>
Write a program that takes two integers as input and performs a right shift operation on the first integer by the number of bits specified by the second integer.

#include <stdio.h>

void main() {

    int a, b;
    
    printf("Enter value a: ");
    scanf("%d", &a);
    printf("Enter value b: ");
    scanf("%d", &b);
    
    printf("%d", a >> b);
}


6. Check if a Bit is Set<br>
Write a program that takes an integer and a bit position as input and checks if the bit at the given position is not zero.

#include <stdio.h>

void main() {

    int num, pos;
    printf("Enter an integer: ");
    scanf("%d", &num);
    printf("Enter the bit position: ");
    scanf("%d", &pos);
    
    if((num & (1 << pos)) != 0) {
        printf("Yes");
    } 
    else {
        printf("No");
    }
}


7. Set a Bit<br>
Write a program that takes an integer and a bit position as input and sets the bit at the given position.

#include <stdio.h>

void setBit(int *num, int position) {

    int mask = 1 << position;
    *num = *num | mask;
}

void main() {

    int num, position;
    printf("Enter value: ");
    scanf("%d", &num);
    printf("Enter bit position: ");
    scanf("%d", &position);

    setBit(&num, position);

    printf("The new value is: %d\n", num);
}


8. Clear a Bit<br>
Write a program that takes an integer and a bit position as input and clears the bit at the given position.

#include <stdio.h>

void main() {

    int num, pos;
    
    printf("Enter value of num: ");
    scanf("%d", &num);
    printf("Enter bit position to clear: ");
    scanf("%d", &pos);
    
    int mask = ~(1 << pos);
    num = num & mask;
    
    printf("Result: %d\n", num);
}


9. Toggle a Bit<br>
Write a program that takes an integer and a bit position as input and toggles the bit at the given position.

#include <stdio.h>

void main() {

    int num, pos;
    
    printf("Enter value of num: ");
    scanf("%d", &num);
    printf("Enter bit position to toggle (0-indexed): ");
    scanf("%d", &pos);
    
    num = num ^ (1 << pos);
    printf("Result: %d", num);
}

<br><br><br><br>

LESSON 5 Strings
<br><br>
Topic 1 String Handling




























