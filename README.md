# Calculator-in-C- By Mohammad Z. Khan
#include <stdio.h>

float add(float x, float y) {
    return x + y;
}

float subtract(float x, float y) {
    return x - y;
}

float multiply(float x, float y) {
    return x * y;
}

float divide(float x, float y) {
    if (y == 0) {
        printf("Error! Division by zero.\n");
        return 0;
    } else {
        return x / y;
    }
}

int main() {
    char choice;
    float num1, num2, result;

    printf("Select operation by choosing number as follows:\n");
    printf("1. For Adding number\n");
    printf("2. for Subtracting number\n");
    printf("3. For Multiplying number\n");
    printf("4. For Dividing number\n");

    while (1) {
        printf("Enter choice by operation ");
        scanf(" %c", &choice);

        if (choice == '1' || choice == '2' || choice == '3' || choice == '4') {
            printf("Enter first number: ");
            scanf("%f", &num1);
            printf("Enter second number: ");
            scanf("%f", &num2);

            switch (choice) {
                case '1':
                    result = add(num1, num2);
                    break;
                case '2':
                    result = subtract(num1, num2);
                    break;
                case '3':
                    result = multiply(num1, num2);
                    break;
                case '4':
                    result = divide(num1, num2);
                    break;
            }
            printf("Result: %.2f\n", result);
        } else {
            printf("Wrong input\n");
        }
    }

    return 0;
}
