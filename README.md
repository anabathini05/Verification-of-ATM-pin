# Verification-of-ATM-pin
#include <stdio.h>

int main() {
    int pin = 1234;       // Correct ATM PIN
    int enteredPin;
    int attempts = 0;

    while(attempts < 3) {
        printf("Enter your ATM PIN: ");
        scanf("%d", &enteredPin);

        if(enteredPin == pin) {
            printf("PIN verified successfully!\n");
            printf("Access granted.\n");
            return 0;
        } 
        else {
            printf("Incorrect PIN. Try again.\n");
            attempts++;
        }
    }

    printf("Too many incorrect attempts. Your card is blocked.\n");

    return 0;
}
