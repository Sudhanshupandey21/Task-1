# Task-1

Task-1(A)


#include <stdio.h>

void addition();
void subtraction();
void multiplication();
void division();

int main() {
    int choice;

    while (1) {
        printf("\nSimple Calculator\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                addition();
                break;
            case 2:
                subtraction();
                break;
            case 3:
                multiplication();
                break;
            case 4:
                division();
                break;
            case 5:
                printf("Exiting...\n");
                return 0;
            default:
                printf("Invalid choice. Please try again.\n");
        }
    }
    return 0;
}

void addition() {
    float num1, num2;
    printf("Enter two numbers to add: ");
    scanf("%f %f", &num1, &num2);
    printf("Result: %.2f\n", num1 + num2);
}

void subtraction() {
    float num1, num2;
    printf("Enter two numbers to subtract: ");
    scanf("%f %f", &num1, &num2);
    printf("Result: %.2f\n", num1 - num2);
}

void multiplication() {
    float num1, num2;
    printf("Enter two numbers to multiply: ");
    scanf("%f %f", &num1, &num2);
    printf("Result: %.2f\n", num1 * num2);
}

void division() {
    float num1, num2;
    printf("Enter two numbers to divide: ");
    scanf("%f %f", &num1, &num2);
    if (num2 != 0)
        printf("Result: %.2f\n", num1 / num2);
    else
        printf("Error: Division by zero is not allowed.\n");
}




Task-2(B)


#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int number, guess, attempts = 0;

    // Seed the random number generator
    srand(time(0));
    // Generate a random number between 1 and 100
    number = rand() % 100 + 1;

    printf("Guess a number between 1 and 100:\n");

    // Loop until the user guesses the correct number
    do {
        printf("Enter your guess: ");
        scanf("%d", &guess);
        attempts++;

        if (guess > number) {
            printf("Too high! Try again.\n");
        } else if (guess < number) {
            printf("Too low! Try again.\n");
        } else {
            printf("Congratulations! You guessed the correct number in %d attempts.\n", attempts);
        }
    } while (guess != number);

    return 0;
}
