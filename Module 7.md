EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:
```
#include<stdio.h>
struct asd{
    int age;
    char name[20];
};
int main()
{
    struct asd p;
    scanf("%d",&p.age);
    scanf("%s",p.name);
    printf("Age:%d\n",p.age);
    printf("Name:%svaccine:%d\n",p.name,p.age);
    if(p.age>18){
       printf("eligibility:yes"); 
    }
    else{
        printf("eligibility:no");
    }
}
```


Output:

![image](https://github.com/user-attachments/assets/e352603d-2a69-4e2e-ade8-c30a9670809e)



Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:

```
#include <stdio.h>
struct Numbers {
    int num1;
    int num2;
    
};
struct Result {
    int sum;
};
struct Result compute(struct Numbers nums) {
    struct Result res;
    res.sum = nums.num1 + nums.num2;
    return res; 
}

int main() {
    struct Numbers nums;
    struct Result res;
    scanf("%d %d ", &nums.num1, &nums.num2);
    res = compute(nums);
    printf("%d\n", res.sum);
    return 0;
}
```




Output:


![image](https://github.com/user-attachments/assets/58bc0409-2242-494f-b52c-f3f6a5b00107)





Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND CREATE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

```
#include <stdio.h>
int main()
{
    char filename[100];
    FILE *fp;
    scanf("%s",filename);
    fp=fopen(filename,"w");
    if(fp!=NULL){
        printf("%s File Created Successfully\n",filename);
        printf("%s File Opened\n",filename);
    }
    fclose(fp);
    printf("%s File Closed",filename);
}
```




Output:


![image](https://github.com/user-attachments/assets/f91eab94-8e78-4687-bb48-2dc7d3a34204)







Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
#include <stdio.h>
int main()
{
   char name[50],ch[100];
   int i,num;
   scanf("%s", name);
   scanf("%d", &num);
   FILE *fptr = fopen(name, "w");
   
  if(fptr == NULL)
  {
      printf("Error!");
      return 1;
  }else{
   printf("%s Opened\n",name);
  }
   for(i = 0; i < num; i++)
   {
      fgets(ch,sizeof(ch),stdin);
      fprintf(fptr,"%s\n",ch);
   }
   fclose(fptr);
   printf("Data added Successfully");
   return 0;
}
```




Output:


![image](https://github.com/user-attachments/assets/332cb406-6b64-4168-99f5-f220ea42cca3)







Result:
Thus, the program is verified successfully



Ex No:5 TO CREATE A STRUCTURE FOR ELECTRICITY BILL CALCULATION USING TYPEDEF & FUNCTION-PASSING STRUCTURE TO A FUNCTION BY VALUE

Aim:
To create a structure for Electricity Bill calculation using typedef & function-Passing structure to a function by value (use service no, name, previous reading, current reading, unit consumption & amount as data members).

Algorithm:
1. Define structure electricityBill with members:
    - sNo (integer)
    - sName (character array)
    - prev (integer)
    - curr (integer)
    - units (integer)
    - amt (float)
2. Declare variable c of type electricityBill.
3. Input service number, service name, current reading, and previous reading using scanf, store in c.sNo, c.sName, c.curr, c.prev.
4. Calculate units consumed: c.units = c.curr - c.prev.
5. If c.units <= 100
    a. Calculate amount: c.amt = c.units * 3.
6. Else if c.units > 100 and c.units <= 300
    a. Calculate amount: c.amt = 300 + (c.units - 100) * 4.
7. Else
    a. Calculate amount: c.amt = 1100 + (c.units - 300) * 5.
8. Print service number, service name, unit consumption, and amount (formatted to 2 decimal places).
9. Return 0.


Program:

```
#include <stdio.h>
typedef struct electricityBill{
    int sNo;
    char sName[20];
    int prev, curr;
    int units;
    float amt;
}eb;
int main(){
    eb c;
    scanf("%d\n%s\n%d\n%d", &c.sNo, c.sName, &c.curr, &c.prev);
    c.units = c.curr - c.prev;
    if(c.units <= 100){
        c.amt = c.units * 3;
    }
    else if(c.units > 100 && c.units <= 300){
        c.amt = 300 + (c.units - 100) * 4;
    }
    else{
        c.amt = 1100 + (c.units - 300) * 5;
    }
    printf("service number:%d\n", c.sNo);
    printf("service name:%s\n", c.sName);
    printf("unit consumption:%d\n", c.units);
    printf("amount:%.2f", c.amt);
}
```

Output:

![image](https://github.com/user-attachments/assets/8eefdd57-e0ba-4494-9758-c97de2f22018)


Result:
Thus, the program is verified successfully
