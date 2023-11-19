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























