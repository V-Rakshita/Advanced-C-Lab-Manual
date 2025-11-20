

# EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
## Aim:
To write a C program to create a function to find the greatest number

## Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
## Program:
```c
#include <stdio.h>

int max_of_four(int a, int b, int c, int d) {
    int max = a;
    if (b > max) max = b;
    if (c > max) max = c;
    if (d > max) max = d;
    return max;
}

int main() {
    int n1, n2, n3, n4;
    printf("Enter four numbers: ");
    if (scanf("%d %d %d %d", &n1, &n2, &n3, &n4) != 4) return 0;
    int greater = max_of_four(n1, n2, n3, n4);
    printf("Greatest number = %d\n", greater);
    return 0;
}
```

## Output:
<img width="409" height="143" alt="image" src="https://github.com/user-attachments/assets/5d56c670-9d4d-4802-ae38-81011b85a72c" />


## Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
# EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
## Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

## Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
## Program:
```c
#include <stdio.h>

void calculate_the_max(int n, int k) {
    int a = 0, o = 0, x = 0;
    for (int i = 1; i < n; i++) {
        for (int j = i + 1; j <= n; j++) {
            int and_val = i & j;
            int or_val  = i | j;
            int xor_val = i ^ j;
            if (and_val < k && and_val > a) a = and_val;
            if (or_val  < k && or_val  > o) o = or_val;
            if (xor_val < k && xor_val > x) x = xor_val;
        }
    }
    printf("%d\n%d\n%d\n", a, o, x);
}

int main() {
    int n, k;
    printf("Enter values of n and k: ");
    if (scanf("%d %d", &n, &k) != 2) return 0;
    calculate_the_max(n, k);
    return 0;
}
```

## Output:
<img width="462" height="200" alt="image" src="https://github.com/user-attachments/assets/f02c2e2f-465d-4420-82e9-4df1ab086916" />


## Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
# EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
## Aim:
To write a C program to write the logic for the requests

## Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
## Program:
```c
#include <stdio.h>

int main() {
    int noshel, noque;
    if (scanf("%d %d", &noshel, &noque) != 2) return 0;

    int shelarr[noshel][1000]; 
    int nobookarr[noshel];
    for (int i = 0; i < noshel; i++) nobookarr[i] = 0;

    for (int q = 0; q < noque; q++) {
        int type, x, y;
        scanf("%d %d %d", &type, &x, &y);
        if (type == 1) {
            shelarr[x][ nobookarr[x] ] = y;
            nobookarr[x]++;
        } else if (type == 2) {
            printf("%d\n", shelarr[x][y]);
        }
    }
    return 0;
}
```

## Output:
<img width="288" height="355" alt="image" src="https://github.com/user-attachments/assets/9bef1a61-4189-4e11-a7bf-7b8623704e90" />



## Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
## Aim:
To write a C program print the sum of the integers in the array.

## Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



## Program:
```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter number of elements: ");
    if (scanf("%d", &n) != 1) return 0;
    int a[n];
    int sum = 0;
    printf("Enter %d integers: ", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
        sum += a[i];
    }
    printf("Sum = %d\n", sum);
    return 0;
}
```

## Output:
<img width="404" height="154" alt="image" src="https://github.com/user-attachments/assets/214e753a-a07f-4112-85aa-ca87f9f812c2" />


 


## Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
# EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE



## Aim:

To write a C program that counts the number of words in a given sentence.

## Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



## Program:
```c
#include <stdio.h>

int main() {
    char sentence[1000];
    int count = 0;
    int i = 0;
    printf("Enter a sentence: ");
    scanf("%[^\n]", sentence);  
    while (sentence[i] != '\0') {
        if (sentence[i] != ' ' &&
           (i == 0 || sentence[i - 1] == ' ')) {
            count++;   
        }
        i++;
    }
    printf("Number of words = %d\n", count);

    return 0;
}
```

## Output:
<img width="513" height="135" alt="image" src="https://github.com/user-attachments/assets/a3bca718-f727-4485-842b-763453e59146" />




## Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
