#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);

    int i = 0, j = strlen(str) - 1;
    int is_palindrome = 1;

    while (i < j) {
        // Compare ignoring case
        if (tolower(str[i]) != tolower(str[j])) {
            is_palindrome = 0;
            break;
        }
        i++;
        j--;
    }

    if (is_palindrome)
        printf("String is a palindrome.\n");
    else
        printf("String is not a palindrome.\n");

    return 0;
}
OUTPUT
Enter a string: madam
String is a palindrome.
string = "madam"

# Convert to lowercase to ignore case sensitivity
string = string.lower()

if string == string[::-1]:
    print("String is a palindrome.")
else:
    print("String is not a palindrome.")
String is a palindrome.
# Check-if-string-is-palindrome
