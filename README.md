# Random-joke-generator
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int choice;

    // List of jokes
    char *jokes[] = {
        "Why don’t programmers like nature? Because it has too many bugs!",
        "Why did the computer go to the doctor? Because it caught a virus!",
        "Why was the math book sad? Because it had too many problems.",
        "Why do programmers prefer dark mode? Because light attracts bugs!",
        "Why did the programmer quit his job? Because he didn’t get arrays!"
    };

    int totalJokes = 5;

    // Seed random number
    srand(time(NULL));

    printf("🎉 Welcome to Random Joke Generator 🎉\n");

    while (1) {
        printf("\nPress 1 to get a joke\n");
        printf("Press 0 to exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        if (choice == 1) {
            int randomIndex = rand() % totalJokes;
            printf("\n😂 Joke:\n%s\n", jokes[randomIndex]);
        } 
        else if (choice == 0) {
            printf("\nThank you for using Random Joke Generator!\n");
            break;
        } 
        else {
            printf("\nInvalid choice! Try again.\n");
        }
    }

    return 0;
}
