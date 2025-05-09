# Impact_T

JAVA 

* Java is a **high-level, object-oriented, platform-independent language** developed by Sun Microsystems.
* Understood the concept of **"Write Once, Run Anywhere" (WORA)** due to Java’s platform independence.
* Wrote and executed a simple Java program using the `main()` method:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

  Class declaration**
  Main method**
  Statements and Syntax**

 Explored **primitive data types** (`int`, `float`, `char`, `boolean`, etc.) and how to declare variables.



* Practiced writing basic Java programs using different data types and print statements.
* Completed exercises using variables, input/output, and operators.



Scanner - class
sc - object
new  Scanner(System.in)- we make reference while run time .while making the reference default method called.
println -next line 
printf()- formatted string ,args

Formated string 
%d - decimal
%f - float
%lf - double 
%e - exponential
%s - string
%S - uppercase string
%o- octal
%x - hexadecimal
%b - Boolean

-precision says by default 6 digit number after decimal
*Escape sequence: used to change the flow of output, sequence character not      printed , but it can change  the flow of output.

-Data Types
.primitive
*integer types
-byte(8bits)
-short(2)
-int(4)
-long(8)

*floating point numbers 
-float(4)
-double(8)

*char type
-char(2)

*Boolean - true,false


.non-primitive

[TYPE CONVERSION]
-WIDENING:lower to higher type(implicit means automatically)
-NARROWING:higher to lower type(explicit means manually)
________________________________________________________________________________________________________________________________________________________________________________________________
📅 Day 1 - Control Statements & Switch Statements
✅ Topics Covered:
Control Flow in Java

if, if-else, if-else-if

[switch Statement]

Comparison between if-else and switch

💡 Key Concepts
🔹 Control Statements in Java
Control statements are used to alter the flow of execution in a program based on conditions. They help implement decision-making and looping behavior.

Types:
Conditional/Decision-making statements – if, if-else, switch

Looping statements – for, while, do-while (covered later)

_______________________________________________________________________________________________________________________________________________________________________________________________________________

📅 Day 2 - Looping in Java
✅ Topics Covered:
Introduction to Loops

for Loop

while Loop

do-while Loop

💡 Key Concepts
🔹 What is Looping?
Looping in Java allows us to execute a block of code repeatedly until a certain condition is met. It is useful for tasks like traversing arrays, repeating tasks, or performing iterations.

🔁 Types of Loops
1. for Loop
Used when the number of iterations is known.
for (int i = 1; i <= 5; i++) {
    System.out.println("Count: " + i);
}

2. while Loop
Used when the condition is checked before each iteration and we don’t necessarily know how many times it will run.
int i = 1;
while (i <= 5) {
    System.out.println("Count: " + i);
    i++;
}

3. do-while Loop
Executes the code at least once, and then continues looping while the condition is true.
int i = 1;
do {
    System.out.println("Count: " + i);
    i++;
} while (i <= 5);
___________________________________________________________________________________________________________________________________________________________________

📅Day 3 - Digit Manipulation & Nested Loops (Patterns)
✅ Topics Covered:
Extracting digits from a number

Reversing a number

Checking for palindrome

Using nested loops to print patterns

Logic building with loops

💡 Key Concepts
🔢 Digit Manipulation
Digit manipulation involves breaking down a number into its individual digits using modulus (%) and division (/) operations.

Example: Reversing a Number
int num = 1234, reverse = 0;
while (num != 0) {
    int digit = num % 10;
    reverse = reverse * 10 + digit;
    num = num / 10;
}
System.out.println("Reversed Number: " + reverse);


Example: Palindrome Check
int original = 121, temp = original, reverse = 0;
while (temp != 0) {
    int digit = temp % 10;
    reverse = reverse * 10 + digit;
    temp = temp / 10;
}
if (original == reverse) {
    System.out.println("Palindrome");
} else {
    System.out.println("Not a palindrome");
}



🔁 Nested Loops & Pattern Printing
Nested loops (a loop inside another loop) are commonly used for printing patterns like triangles, pyramids, and rectangles.

Example 1: Right-Angle Triangle Pattern
for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print("* ");
    }
    System.out.println();
}
Output:
* 
* * 
* * * 
* * * * 
* * * * * 


Example 2: Inverted Number Pyramid
for (int i = 5; i >= 1; i--) {
    for (int j = 1; j <= i; j++) {
        System.out.print(j + " ");
    }
    System.out.println();
}
Output:
1 2 3 4 5 
1 2 3 4 
1 2 3 
1 2 
1 
___________________________________________________________________________________________________________________________________________________________________


📅 Day 4 – 08 May
🧩 Patterns & Number Problems
✅ Topics Covered:
Advanced Pattern Printing using nested loops

Number-based logic building

Solving classic number problems using loops and conditions:

Sum of digits

💡 Key Concepts
🔹 Pattern Printing (Advanced)
Example: Number Pyramid Pattern

for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print(j + " ");
    }
    System.out.println();
}
Output:

Copy
Edit
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5 
Example: Floyd’s Triangle


int num = 1;
for (int i = 1; i <= 4; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print(num + " ");
        num++;
    }
    System.out.println();
}
Output:

Copy
Edit
1 
2 3 
4 5 6 
7 8 9 10 

🔢 Number Problems
Sum of Digits:

int num = 1234, sum = 0;
while (num != 0) {
    sum += num % 10;
    num /= 10;
}
System.out.println("Sum: " + sum);


NESTED LOOPS
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter number: ");
        int rows = scanner.nextInt();
        scanner.close();

        
        for (int i = 1; i <= rows; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
        
            System.out.println();
        }
    }
}




----import java.util.Scanner;

public class StaircasePattern {
    public static void main(String[] args) {
        int n=4;
        for (int i = 0; i <= n; i++) {
           
            for (int j = 0; j <i; j++) {
                System.out.print(" ");
            }
           
            for (int k = 0; k<n-i;k++) 
            {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}

-----public class Main{
    public static void main(String[] args) {
        int n = 4; 

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
               
                if (i == 1 || i == n || j == 1 || j == n) 
                {
                    System.out.print("* ");
                } 
                else 
                {
                    System.out.print("  "); 
                }
            }
            System.out.println(); 
        }
    }
}


* * * * 
*       * 
*       * 
* * * *



 
-----public class Main{
    public static void main(String[] args) {
        int n = 5; 

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
               
                if (i == 0 || i == n-1 || j == 0|| j == n-1) 
                {
                    System.out.print("* ");
                } 
                else 
                {
                    System.out.print("  "); 
                }
            }
            System.out.println(); 
        }
    }
}
___________________________________________________________________________________________

📅 Day 5 – Arrays in Java
✅ Topics Covered:
Introduction to Arrays

Declaring, initializing, and accessing array elements

One-dimensional (1D) arrays

Traversing arrays using loops

Basic array operations: sum, max, min, search

💡 Key Concepts
🔹 What is an Array?
An array is a data structure that stores multiple values of the same data type in a single variable. Arrays are used to handle large amounts of data efficiently.

🔹 Declaring and Initializing a 1D Array:

int[] numbers = new int[5];  // declaration
numbers[0] = 10;             // initialization

// or directly
int[] values = {10, 20, 30, 40, 50};
🔹 Traversing an Array:
for (int i = 0; i < values.length; i++) {
    System.out.println("Element at index " + i + ": " + values[i]);
}



🔢 Basic Array Operations

Sum of All Elements:
int sum = 0;
for (int i = 0; i < values.length; i++) {
    sum += values[i];
}
System.out.println("Sum = " + sum);


Finding Maximum Element:
int max = values[0];
for (int i = 1; i < values.length; i++) {
    if (values[i] > max)
        max = values[i];
}
System.out.println("Maximum = " + max);



Searching an Element:
int search = 30, found = -1;
for (int i = 0; i < values.length; i++) {
    if (values[i] == search) {
        found = i;
        break;
    }
}
System.out.println((found != -1) ? "Found at index " + found : "Not found");


🔹 Introduction to 2D Arrays
A two-dimensional array is like a table (rows and columns).
int[][] matrix = {
    {1, 2},
    {3, 4}
};

// Access element
System.out.println(matrix[0][1]);  // Output: 2

Declared and initialized 1D arrays

Wrote code to find sum, average, and maximum element of an arra
Scanner sc = new Scanner(System.in);
int n =sc.nextInt();
int arr[]=new int[n];
for (int i=0;i<n;i++){
arr[i]= sc.nextInt();
}
for (int i=0;i<n;i++){

}



import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n=sc.nextInt();
        int arr[]=new int[n];
        for(int i =0;i<n;i++)
        {
            arr[i]=sc.nextInt();
            System.out.print(arr[i]+" ");
        }
    }
    
}
        

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter array size:");
        int n=sc.nextInt();
        int arr[]=new int[n];
        System.out.println("eneter elements:");
        for(int i =0;i<n;i++)
        {
            arr[i]=sc.nextInt();
        }
        int sum=0;
        System.out.println("elements in array:");
        for(int i =0;i<n;i++)
        {
            sum+=arr[i];
            System.out.print(arr[i]+" ");
        }
        System.out.println("sum"+sum);
    }
    
}
___________________________________________________________________________________________________________________________________________________________________________________________

📅 Day 5 – Arrays in Java
✅ Topics Covered:
Introduction to Arrays

Declaring, initializing, and accessing array elements

One-dimensional (1D) arrays

Traversing arrays using loops

Basic array operations: sum, max, min, search

💡 Key Concepts
🔹 What is an Array?
An array is a data structure that stores multiple values of the same data type in a single variable. Arrays are used to handle large amounts of data efficiently.

🔹 Declaring and Initializing a 1D Array:

int[] numbers = new int[5];  // declaration
numbers[0] = 10;             // initialization

// or directly
int[] values = {10, 20, 30, 40, 50};


🔹 Traversing an Array:
for (int i = 0; i < values.length; i++) {
    System.out.println("Element at index " + i + ": " + values[i]);
}

🔢 Basic Array Operations

Sum of All Elements:
int sum = 0;
for (int i = 0; i < values.length; i++) {
    sum += values[i];
}
System.out.println("Sum = " + sum);


Finding Maximum Element:
int max = values[0];
for (int i = 1; i < values.length; i++) {
    if (values[i] > max)
        max = values[i];
}
System.out.println("Maximum = " + max);
Searching an Element:
int search = 30, found = -1;
for (int i = 0; i < values.length; i++) {
    if (values[i] == search) {
        found = i;
        break;
    }
}
System.out.println((found != -1) ? "Found at index " + found : "Not found");



🔹 Introduction to 2D Arrays
A two-dimensional array is like a table (rows and columns).
int[][] matrix = {
    {1, 2},
    {3, 4}
};
// Access element
System.out.println(matrix[0][1]);  // Output: 2




Declared and initialized 1D arrays

Wrote code to find sum, average, and maximum element of an arra
Scanner sc = new Scanner(System.in);
int n =sc.nextInt();
int arr[]=new int[n];
for (int i=0;i<n;i++){
arr[i]= sc.nextInt();
}
for (int i=0;i<n;i++){

}



import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n=sc.nextInt();
        int arr[]=new int[n];
        for(int i =0;i<n;i++)
        {
            arr[i]=sc.nextInt();
            System.out.print(arr[i]+" ");
        }
    }
    
}
        




