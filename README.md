#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <string.h>
int main() {
    char choice[10], result[10];
    int random_num;
    srand(time(NULL));
    printf("Welcome to Coin Toss!\n");
    printf("Choose 'heads' or 'tails': ");
    scanf("%s", choice);
    if (strcmp(choice, "heads") != 0 && strcmp(choice, "tails") != 0) {
        printf("Invalid choice. Please choose 'heads' or 'tails'.\n");
        return 1;
    }
    random_num = rand() % 2;
    if (random_num == 0) {
        strcpy(result, "heads");
    } else {
        strcpy(result, "tails");
    }
    if (strcmp(choice, result) == 0) {
        printf("The coin landed on %s. You win!\n", result);
    } else {
        printf("The coin landed on %s. You lose.\n", result);
    }
    return 0;
}
