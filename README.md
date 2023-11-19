# CodeChum_Study_Area_Exercises
Programming Course 1 CodeChum Exercises

Lesson 3 Input/Output

Topic 1 Output Operations
1. Hello World
Write a program that prints the string "Hello, World!" to the console.

#include <stdio.h>

void main() {

    printf("Hello, World!");
}

2. Odd or Even
Write a program that takes an integer as input and prints whether the number is odd or even.

#include <stdio.h>

void main() {

    int n;

    printf("Enter an integer: ");
    scanf("%d", &n);

    if(n%2 == 0) printf("%d is even.", n);
    else printf("%d is odd.", n);
}


