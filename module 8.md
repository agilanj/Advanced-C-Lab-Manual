EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER

Aim:
To write a C program print the lowercase English word corresponding to the number

Algorithm:

1.Start the program.
2.Include the header file stdio.h.

3.Begin the main function.

4.Declare an integer variable n to store user input.

5.Read an integer from the user using scanf and store it in variable n.

6.Check if n is between 21 and 29 (inclusive):

7.If yes, use a switch statement to match the value of n.

8.For each case (21 to 29), print the corresponding English word in lowercase.

9.If n is greater than 29, print the message "Greater than 29".

10.End the main function and return 0.
 
Program:

```
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);
    if (n >= 21 && n <= 29) {
        switch (n) { 
            case 21: printf("twenty one\n"); break;
            case 22: printf("twenty two\n"); break;
            case 23: printf("twenty three\n"); break;
            case 24: printf("twenty four\n"); break;
            case 25: printf("twenty five\n"); break;
            case 26: printf("twenty six\n"); break;
            case 27: printf("twenty seven\n"); break;
            case 28: printf("twenty eight\n"); break;
            case 29: printf("twenty nine\n"); break;
        }
    } else if (n > 29) {
        printf("Greater than 29\n");
    }

    return 0;
}

```




Output:

![image](https://github.com/user-attachments/assets/846ded75-3c64-4886-bb8a-2945f9490141)







Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include <stdio.h>
#include <string.h>
int main() {
    char str[1001];  
    int freq[10] = {0}; 
    scanf("%s", str);
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= '0' && str[i] <= '9') {
            freq[str[i] - '0']++; 
        }
    }
    for (int i = 0; i < 10; i++) {
        printf("%d ", freq[i]);
    }
    printf("\n");
    return 0;
}
```




Output:


![image](https://github.com/user-attachments/assets/0c28e3bd-6605-4a65-89fa-621a87a27ea1)







Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
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
 
Program:

```
# include <stdio.h>
# include <string.h>
# include <stdbool.h>
void swap(char *a,char *b)
{
    char temp[100];
    strcpy(temp,a);
    strcpy(a,b);
    strcpy(b,temp);
}
bool permutation(char a[][100],int n)
{
    int k = -1;
    int l;
    for(int i=0;i<n-1;i++)
    {
        if(strcmp(a[i],a[i+1]) <0)
        {
            k = i;
        }
    }
    if(k==-1)
    {
        return false;
    }
    for(int i=k+1;i<n;i++)
    {
        if(strcmp(a[k],a[i]) < 0)
        {
            l = i;
        }
    }
    swap(a[k],a[l]);
    
    for(int i=k+1,j=n-1;i<j;i++,j--)
    {
        swap(a[i],a[j]);
    }
    return true;
}
int main()
{
    int n;
    scanf("%d",&n);
    char a[n][100];
    for(int i=0;i<n;i++)
    {
        scanf("%s",a[i]);
    }
    
    do{
        for(int i=0;i<n;i++)
        {
            printf("%s ",a[i]);
        }
        printf("\n");
    }while(permutation(a,n));
    
}

```


Output:


![image](https://github.com/user-attachments/assets/b0b68809-2985-4cc0-a969-4658ff178b8c)







Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

```
#include<stdio.h>
int main()
{
    int n,s=0;
    scanf("%d",&n);
    int l=2*n-1;
    int e=l-1;
    int a[l][l];
    while(n!=0)
    {
        for(int i=s;i<=e;i++)
        {
            for(int j=s;j<=e;j++)
            {
                if(i==s || i==e || j==s|| j==e){
                    a[i][j]=n;
                }
            }
        }
        s++;
        e--;
        n--;
    }
    for(int i=0;i<l;i++)
    {
        for(int j=0;j<l;j++)
        {
            printf("%d ",a[i][j]);
        }
        printf("\n");
    }
}
```




Output:


![image](https://github.com/user-attachments/assets/2ae72e10-adab-4307-928a-badc9c8e8095)






Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY. 

Aim:

To write a C program that calculates the sum of integers in the array

Algorithm:

1.Start the program.

2.Include the header file stdio.h.

3.Begin the main function.

4.Declare an integer variable n to store the number of elements.

5.Declare an integer variable sum and initialize it to 0.

6.Read the value of n (number of array elements) using scanf.

7.Declare an integer array a of size n.

8.Use a for loop that runs from i = 0 to i < n:

In each iteration:

Read an integer into a[i] using scanf.

Add a[i] to sum.

9.After the loop ends, print the value of sum.

10.End the main function.

Program:
```
#include<stdio.h>
int main(){
    int n,sum=0;
    scanf("%d",&n);
    int a[n];
    for(int i=0;i<n;i++){
        scanf("%d",&a[i]);
        sum+=a[i];
    }
    printf("%d",sum);
    
}

```


Output:

![image](https://github.com/user-attachments/assets/5f8db9e2-b5ba-4eb6-885b-e87439ccbb4f)







Result:
Thus, the program is verified successfully



























