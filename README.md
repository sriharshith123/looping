#include <stdio.h>
#include <ctype.h>

int main() {
    char str[100];
    int counts[5] = {0}; // Array to store counts of each category
    
    printf("Enter a string: ");
    fgets(str, 100, stdin);
    
    for(int i = 0; str[i] != '\0'; i++) {
        char c = str[i];
        if(isupper(c))
            counts[0]++;
        else if(islower(c))
            counts[1]++;
        else if(isdigit(c))
            counts[2]++;
        else if(isspace(c))
            counts[3]++;
        else
            counts[4]++;
    }
    
    printf("Uppercase characters: %d\n", counts[0]);
    printf("Lowercase characters: %d\n", counts[1]);
    printf("Digits: %d\n", counts[2]);
    printf("Whitespace characters: %d\n", counts[3]);
    printf("Special symbols: %d\n", counts[4]);
    
    return 0;
}
