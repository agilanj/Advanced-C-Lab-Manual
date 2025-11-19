

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER

Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1. Define the function max_of_four() with four integer parameters: a, b, c, d.
2. Compare a, b, c, and d:
    a. If a is greater than b, c, and d, return a.
    b. Else if b is greater than a, c, and d, return b.
    c. Else if c is greater than a, b, and d, return c.
    d. Else return d.
3. In main():
    a. Declare four integer variables a, b, c, d.
    b. Read four integers from input using scanf.
    c. Call max_of_four(a, b, c, d) and store the result in max.
    d. Print max.

 
Program:

```
#include <stdio.h>

int max_of_four(int a, int b, int c, int d){
    if(a > b && a > c && a > d) return a;
    else if(b > a && b > c && b > d) return b;
    else if(c > a && c > b && c > d) return c;
    else return d;
}

int main(){
    int a, b, c, d;
    scanf("%d\n%d\n%d\n%d", &a, &b, &c, &d);
    int max = max_of_four(a, b, c, d);
    printf("%d", max);
}
```

Output:

![image](https://github.com/user-attachments/assets/011ca694-9749-4407-b079-d823e6ef4c6d)


Result:
Thus, the program is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS

Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1. Define the function calculate_the_maximum() with two integer parameters: n and k.
2. Initialize three integers max_and, max_or, max_xor to 0.
3. Declare temporary integers a, b, c for bitwise operations.
4. Use nested loops:
    a. Outer loop i runs from 1 to n-1.
    b. Inner loop j runs from i+1 to n.
5. For each pair (i, j):
    a. Calculate a = i & j (bitwise AND).
    b. Calculate b = i | j (bitwise OR).
    c. Calculate c = i ^ j (bitwise XOR).
6. Update max_and if a > max_and and a < k.
7. Update max_or if b > max_or and b < k.
8. Update max_xor if c > max_xor and c < k.
9. After loops end, print max_and, max_or, and max_xor.
10. In main():
    a. Read integers n and k from input.
    b. Call calculate_the_maximum(n, k).

Program:

```
#include <stdio.h>

void calculate_the_maximum(int n, int k){
    int max_and = 0;
    int max_or = 0;
    int max_xor = 0;
    int a = 0, b = 0, c = 0;
    for(int i = 1; i < n; i++){
        for(int j = i + 1; j <= n; j++){
            a = i & j;
            b = i | j;
            c = i ^ j;
            if(a > max_and && a < k) max_and = a;
            if(b > max_or && b < k) max_or = b;
            if(c > max_xor && c < k) max_xor = c;
        }
    }
    printf("%d\n%d\n%d\n", max_and ,max_or, max_xor);
}

int main(){
    int n, k;
    scanf("%d %d", &n, &k);
    
    calculate_the_maximum(n, k);
}
```

Output:

![image](https://github.com/user-attachments/assets/06204d53-caf3-4077-93ce-8b8cff693a34)


Result:
Thus, the program is verified successfully.


 
EXP NO:23 C PROGRAM TO FIND A TERM, WHERE THE NEXT TERM IS SUM OF PERVIOUS THREE TERMS IN THE SEQUENCE
Aim:
To write a C program to find a term, where the next term is sum of previous three terms in the sequence.

Algorithm:
1. Define a function series() with four integer parameters: n, a, b, c.
2. If n equals 4:
    a. Print the sum of a, b, and c.
    b. Return from the function.
3. Else:
    a. Recursively call series() with parameters (n-1, b, c, a + b + c).
4. In main():
    a. Declare integer n.
    b. Read integer n from input.
    c. Declare integers a, b, c.
    d. Read integers a, b, c from input.
    e. Call series(n, a, b, c).

Program:

```
#include <stdio.h>
#include <string.h>

void series(int n,int a, int b, int c){
    if(n == 4){
        printf("%d", a + b + c);
        return;
    }
    series(n - 1, b, c, a + b + c);
}

int main(){
    int n;
    scanf("%d\n", &n);
    int a, b, c;
    scanf("%d %d %d", &a, &b, &c);
    series(n, a, b, c);
}
```

Output:

![image](https://github.com/user-attachments/assets/a7c6cb7a-ed1a-4305-b0d6-e6c9b57ac229)


Result:
Thus, the program is verified successfully.


 
EXP NO:24 PROGRAM TO CONVERT UPPERCASE TO LOWERCASE WITHOUT USING THE INBUILT FUNCTION.

Aim:
To write a C program to convert uppercase to lowercase without build in function.

Algorithm:
1. Declare a character array str of size 20.
2. Read a line of input (including spaces) into str using scanf.
3. Loop through each character in str until the null terminator:
    a. If the character is uppercase (between 'A' and 'Z'):
        i. Convert it to lowercase by adding 32.
4. Print the modified string str.

Program:

```
#include <stdio.h>
#include <string.h>

int main(){
    char str[20];
    scanf("%[^\n]%*c", str);
    for(int i = 0; str[i] != '\0'; i++){
        if('A' <= str[i] && str[i] <= 'Z'){
            str[i] = (str[i] + 32);
        }
    }
    printf("%s", str);
}
```

Output:

![image](https://github.com/user-attachments/assets/7d6e1756-5009-4034-a8be-68edaa3d90dd)

Result:
Thus, the program is verified successfully.


 
EXP NO 25: C PROGRAM TO REVERSE A STRING

Aim:

To write a C program that reverses a string.

Algorithm:

1. Include standard input-output and string header files.
2. Define the function reverse() with a character pointer parameter s.
3. Calculate the length n of string s using strlen().
4. Declare a character array sr of size n.
5. Print the input string s.
6. Loop from i = 0 to i < n:
    a. Assign sr[i] = s[n - i - 1] to reverse the string.
7. Set sr[n] = '\0' to terminate the reversed string.
8. Print the reversed string sr.
9. In main():
    a. Declare a character array str of size 20.
    b. Read a line of input including spaces into str using scanf.
    c. Call reverse(str).


Program:

```
#include <stdio.h>
#include <string.h>

void reverse(char *s){
    int n = strlen(s);
    char sr[n];
    printf("Input String: %s\n", s);
    for(int i = 0; i < n; i++){
        sr[i] = s[n - i - 1];
    }
    sr[n] = '\0';
    printf("Reverse String: %s\n", sr);
}

int main(){
    char str[20];
    scanf("%[^\n]%*c", str);
    reverse(str);
}
```

Output:

![image](https://github.com/user-attachments/assets/2e567b24-0df3-45c2-8093-eba339706e26)


Result:

Thus, the program is verified successfully.
