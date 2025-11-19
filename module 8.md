# EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
## Aim:
To write a C program print the lowercase English word corresponding to the number
## Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
## Program:

```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);

    switch(n) {
        case 5:  printf("seventy one\n"); break;
        case 6:  printf("seventy two\n"); break;
        case 7:  printf("seventy three\n"); break;
        case 8:  printf("seventy four\n"); break;
        case 9:  printf("seventy five\n"); break;
        case 10: printf("seventy six\n"); break;
        case 11: printf("seventy seven\n"); break;
        case 12: printf("seventy eight\n"); break;
        case 13: printf("seventy nine\n"); break;
        default: printf("Greater than 13\n");
    }

    return 0;
}
```




## Output:
<img width="360" height="198" alt="image" src="https://github.com/user-attachments/assets/05246805-5b8d-4397-a465-44b26cd68f01" />






## Result:
Thus, the program is verified successfully
 
# EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
## Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
## Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
## Program:

```c
#include <stdio.h>
#include <string.h>

int main() {
    char a[50];
    int count[4] = {0, 0, 0, 0};

    printf("Enter a string of digits: ");
    scanf("%s", a);

    for(int i = 0; i < strlen(a); i++) {
        if(a[i] >= '0' && a[i] <= '3') {
            count[a[i] - '0']++;
        }
    }

    for(int i = 0; i < 4; i++) {
        printf("%d ", count[i]);
    }
    printf("\n");

    return 0;
}
```




## Output:

<img width="631" height="250" alt="image" src="https://github.com/user-attachments/assets/338c9998-85e8-4ae2-a936-7015626553d6" />







## Result:
Thus, the program is verified successfully

# EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
## Aim:
To write a C program to print all of its permutations in strict lexicographical order.

## Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
## Program:
```c
#include <stdio.h>
#include <string.h>

int next_permutation(int n, char *s)
{
    int k, l;
    for (k = n - 2; k >= 0; k--)
    {
        if (s[k] < s[k + 1]) break;
    }
    if (k < 0) return 0;

    for (l = n - 1; l > k; l--)
    {
        if (s[k] < s[l]) break;
    }

    char tmp = s[k];
    s[k] = s[l];
    s[l] = tmp;

    for (int i = k + 1, j = n - 1; i < j; i++, j--)
    {
        tmp = s[i];
        s[i] = s[j];
        s[j] = tmp;
    }
    return 1;
}

int main()
{
    char s[100];
    printf("Enter a string: ");
    scanf("%s", s);

    int n = strlen(s);

    for (int i = 0; i < n - 1; i++)
        for (int j = i + 1; j < n; j++)
            if (s[i] > s[j])
            {
                char tmp = s[i];
                s[i] = s[j];
                s[j] = tmp;
            }

    printf("\nAll permutations in lexicographical order:\n");
    do
    {
        printf("%s\n", s);
    } while (next_permutation(n, s));

    return 0;
}
```





## Output:

<img width="602" height="394" alt="image" src="https://github.com/user-attachments/assets/54b55cf3-5959-44da-be63-0ffe4d4ca6ab" />







## Result:
Thus, the program is verified successfully
 
# EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW.
## Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
## Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
## Program:

```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter n: ");
    scanf("%d", &n);

    int len = n * 2 - 1;

    for (int i = 0; i < len; i++) {
        for (int j = 0; j < len; j++) {
            int min = i < j ? i : j;
            min = min < (len - 1 - i) ? min : (len - 1 - i);
            min = min < (len - 1 - j) ? min : (len - 1 - j);
            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
```





## Output:


<img width="617" height="516" alt="image" src="https://github.com/user-attachments/assets/8f50c0d4-009c-442d-aafe-b16954f63130" />






## Result:
Thus, the program is verified successfully

## EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

## Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

## Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

## Program:

```c
#include <stdio.h>

int square() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;
}

int main() {
    int result = square();
    printf("Square: %d\n", result);
    return 0;
}
```




## Output:


<img width="453" height="223" alt="image" src="https://github.com/user-attachments/assets/e10c7cd5-1fdf-4bbe-b9ab-15487ffadeb1" />







## Result:
Thus, the program is verified successfully



























