# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    float length, breadth, area;
    float *l = &length, *b = &breadth;
    scanf("%f %f", l, b);
    area = (*l) * (*b);
    printf("%.2f\n", area);
    return 0;
}
## OUTPUT
10 5
50.00


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    char *str = (char *)malloc(8 * sizeof(char));
    strcpy(str, "WELCOME");
    printf("%s\n", str);
    free(str);
    return 0;
}
## OUTPUT
WELCOME


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
#include <stdio.h>

struct Student {
    int roll;
    char name[50];
    float marks;
};

int main() {
    struct Student s;
    scanf("%d %s %f", &s.roll, s.name, &s.marks);
    printf("%d %s %.2f\n", s.roll, s.name, s.marks);
    return 0;
}

## OUTPUT
101 Aishwarya 89.5
101 Aishwarya 89.5

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
#include <stdio.h>

struct Employee {
    int id;
    char name[50];
    float basic, hra, da, gross;
};

int main() {
    struct Employee e[3];
    int i;
    for (i = 0; i < 3; i++)
        scanf("%d %s %f %f %f", &e[i].id, e[i].name, &e[i].basic, &e[i].hra, &e[i].da);
    for (i = 0; i < 3; i++) {
        e[i].gross = e[i].basic + e[i].hra + e[i].da;
        printf("%d %s %.2f\n", e[i].id, e[i].name, e[i].gross);
    }
    return 0;
}

 ## OUTPUT
101 Aishwarya 20000 5000 3000
102 Ravi 18000 4000 2500
103 Meena 22000 6000 3500
 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
#include <stdio.h>

struct Student {
    int marks[5];
    int total;
    float average;
};

int main() {
    struct Student s;
    int i;
    s.total = 0;
    for (i = 0; i < 5; i++) {
        scanf("%d", &s.marks[i]);
        s.total += s.marks[i];
    }
    s.average = s.total / 5.0;
    printf("%d %.2f\n", s.total, s.average);
    return 0;
}

## OUTPUT
80 75 90 85 70
400 80.00 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


