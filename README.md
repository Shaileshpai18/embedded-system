DAY - 1 

 

1.//Write a program in c to calculate the area of the triangle 

  #include <stdio.h> 

  int main() 

  { 

    float b,h,area; 

    b=13; 

    h=14; 

    area=(b*h)/2; 

    printf("area of the triangle is\n"); 

    return 0; 

   } 

 

2.// Write a program to find the largest of three numbers using ternary operator  

  #include <stdio.h> 

  int main()  

  { 

    int a = 5, b = 10, c = 15, result; 

    result = (a > b) ? (a > c ? a : c) : (b > c ? b : c); 

    printf("Largest number among %d, %d and %d is %d", a,b,c,result); 

    return 0; 

   } 

 

3.// Write a program to calculate the distance between two points use math.h to compute sqrt and power 

  #include <stdio.h> 

  #include <math.h> 

  int main()  

  { 

    double a, b, x, y, distance; 

    printf("Enter the coordinates of the first point (a b)"); 

    scanf("%lf %lf", &a, &b); 

    printf("Enter the coordinates of the second point (x y)"); 

    scanf("%lf %lf", &x, &y); 

    distance = sqrt(pow(x - a, 2) + pow(y - b, 2)); 

    printf("The distance between the two points is: %lf\n", distance); 

    return(0); 

  } 

 

4.//Ramesh’s basic salary is input through the keyboard, His DA is 40% of basic, and HRA is 20% of basic. Compute his gross salary. 

  #include <stdio.h> 

  int main()  

  { 

    float basic_salary, da, hra, gross_salary; 

    printf("Enter Ramesh's basic salary"); 

    scanf("%f", &basic_salary); 

    da = 0.40 * basic_salary; 

    hra = 0.20 * basic_salary; 

    gross_salary = basic_salary + da + hra; 

    printf("Ramesh's gross salary is: %.2f\n", gross_salary); 

    return(0); 

  } 

 

5.// If a five digit number is input through the keyboard, write a program to reverse the number. 

  #include <stdio.h> 

  int main()  

  { 

    int number, reverse = 0; 

    printf("Enter a five-digit number: "); 

    scanf("%d", &number); 

    if (number < 10000 || number > 99999) { 

        printf("Please enter a valid five-digit number.\n"); 

        return 1; 

    } 

    while (number != 0) { 

        reverse = reverse * 10 + number % 10; 

        number = number / 10; 

    } 

    printf("The reversed number is: %d\n", reverse); 

    return(0); 

   } 

 

DAY-2 

 

1.#include<stdio.h> //preprocessor directive 

int main() 

{ 

    int h; //variable declaration 

    printf("enter the heignt in cms"); //input 

    scanf("%d",&h);  //computation keyword 

    printf("your height is %d",h); //output 

    return 0; 

} 

 

2.#include<stdio.h> 

void main() 

{ 

    int a=3; 

    int b=++a + a++ + --a; 

    printf("value of b is %d",b); 

} 

output= b=13 

 

3.ternary operator :- exp? exp2: exp3 

#include<stdio.h> 

void main() 

{ 

    int a; 

    printf("enter your age"); 

    scanf("%d",&a); 

    (a>18)?printf("older than 18"):printf("not older than 18"); 

} 

 

4.//design a c program to find the radius of a solid sphere of metal cast by melting a cubiod of dimension l,b,h where l,b and h are user input. 

#include <stdio.h> 

#include <math.h> 

 

int main() { 

    double l, b, h, volume_cuboid, volume_sphere, radius; 

    printf("Enter the length (l) of the cuboid: "); 

    scanf("%lf", &l); 

    printf("Enter the breadth (b) of the cuboid: "); 

    scanf("%lf", &b); 

    printf("Enter the height (h) of the cuboid: "); 

    scanf("%lf", &h); 

    volume_cuboid = l * b * h; 

    volume_sphere = volume_cuboid; 

    radius = cbrt((3 * volume_sphere) / (4 * M_PI)); 

    printf("The radius of the sphere is: %.2lf\n", radius); 

 

    return 0; 

} 

 

5.//design c program to find reminder after division without using mod operator. 

#include <stdio.h> 

int main() { 

    int dividend, divisor, quotient, remainder; 

    printf("Enter the dividend: "); 

    scanf("%d", &dividend); 

    printf("Enter the divisor: "); 

    scanf("%d", &divisor); 

    quotient = dividend / divisor; 

    remainder = dividend - (quotient * divisor); 

    printf("Remainder after division is: %d\n", remainder); 

    return 0; 

} 

 

6.//write a c program that takes the marks of a student in five subjects as input.calculate the average and use relational and logical operators to assign a grade:                                                          

a.for average >=90 

b.for average >=75 and <90 

c.for average >=50 and <75 

d.for average <50 

#include <stdio.h> 

int main()  

{ 

    float marks[5]; 

    float total = 0, average; 

    char grade; 

    printf("Enter the marks for five subjects:\n"); 

    for (int i = 0; i < 5; i++) { 

        printf("Subject %d: ", i + 1); 

        scanf("%f", &marks[i]); 

        total += marks[i]; 

    } 

    average = total / 5; 

    if (average >= 90) { 

        grade = 'A'; 

    } else if (average >= 75 && average < 90) { 

        grade = 'B'; 

    } else if (average >= 50 && average < 75) { 

        grade = 'C'; 

    } else if (average < 50) { 

        grade = 'D'; 

    } else { 

        grade = 'F'; 

    } 

    printf("\nTotal Marks: %.2f\n", total); 

    printf("Average Marks: %.2f\n", average); 

    printf("Grade: %c\n", grade); 

    return 0; 

} 

 

7.//write a c program that calculate the final price of items in a shopping cart after applying a discount.the program should take the original price and discount percentage as inputs.if the discount is >50%,set it to 50% using conditional operator. 

#include <stdio.h> 

int main() { 

    float originalPrice, discountPercentage, finalPrice; 

    printf("Enter the original price of the item: "); 

    scanf("%f", &originalPrice); 

    printf("Enter the discount percentage: "); 

    scanf("%f", &discountPercentage); 

    discountPercentage = (discountPercentage > 50) ? 50 : discountPercentage; 

    finalPrice = originalPrice * (1 - discountPercentage / 100); 

    printf("The final price after applying the discount is: %.2f\n", finalPrice); 

    return 0; 

} 

 

8.//write a c program that takes the user's age as input and check if the user is eligible to vote. the program should also determine if the user is eligible to run for a public office. the rel ational and logical operator to evaluate the conditions and print appropriate messages.  

#include <stdio.h> 

int main()  

{ 

    int age; 

    printf("Enter your age: "); 

    scanf("%d", &age); 

    if (age >= 18) { 

        printf("You are eligible to vote.\n"); 

        if (age >= 25) { 

            printf("You are eligible to run for public office.\n"); 

        } else { 

            printf("You are not eligible to run for public office.\n"); 

        } 

    } else { 

        printf("You are not eligible to vote.\n"); 

        printf("You are not eligible to run for public office.\n"); 

    } 

    return 0; 

} 

 

9.//write a c program that takes three integer input from the user and determine whether all three numbers are equal,any two number are equal ,or all are different also,check if all numbers are positive using  logical operators. 

#include <stdio.h> 

int main()  

{ 

    int num1, num2, num3; 

    printf("Enter the first number: "); 

    scanf("%d", &num1); 

    printf("Enter the second number: "); 

    scanf("%d", &num2); 

    printf("Enter the third number: "); 

    scanf("%d", &num3); 

    if (num1 > 0 && num2 > 0 && num3 > 0) { 

        printf("All numbers are positive.\n"); 

    } else { 

        printf("Not all numbers are positive.\n"); 

    } 

    if (num1 == num2 && num2 == num3) { 

        printf("All three numbers are equal.\n"); 

    } 

    else if (num1 == num2 || num2 == num3 || num1 == num3) { 

        printf("Any two numbers are equal.\n"); 

    } 

    else { 

        printf("All numbers are different.\n"); 

    } 

    return 0; 

} 

 

10.//design a c program to find cost of painting a wall on five slides that is built from k bricks of length l,b,h.only length l and b, length and breath of wall are known from user inputs. cost of painting a unit square is equal to value of pi. 

#include <stdio.h> 

#define PI 3.14159265358979323846 

int main()  

{ 

    int k;              

    double l, b, h;  

    double L, B;         

    double area, cost;   

    printf("Enter the number of bricks (k): "); 

    scanf("%d", &k); 

    printf("Enter the length (l), breadth (b), and height (h) of a brick: "); 

    scanf("%lf %lf %lf", &l, &b, &h); 

    printf("Enter the length (L) and breadth (B) of the wall: "); 

    scanf("%lf %lf", &L, &B); 

    area = 2 * (L * B + L * h + B * h); 

    cost = area * PI; 

    printf("Total area to be painted: %.2lf square units\n", area); 

    printf("Cost of painting the wall: %.2lf units\n", cost); 

    return 0; 

} 

 

11.//Write a C program to calculate the electricity bill for a household. The program should take the number of units consumed as input and apply the following tariff: 

 

For the first 100 units: $1.50 per unit 

 

For the next 200 units: $2.00 per unit 

 

Above 300 units: $3.00 per unit 

 

Use conditional operators to apply the correct tariff based on the units consumed. 

#include <stdio.h> 

int main() { 

    int units; 

    double bill; 

    printf("Enter the number of units consumed: "); 

    scanf("%d", &units); 

    bill = (units <= 100) ? (units * 1.50) : 

           (units <= 300) ? (100 * 1.50 + (units - 100) * 2.00) : 

           (100 * 1.50 + 200 * 2.00 + (units - 300) * 3.00); 

    printf("Electricity Bill: $%.2lf\n", bill); 

    return 0; 

} 

 

DAY - 3 

 

If (text expression) 

{ 

  statement 1; 

  . 

  . 

  statement n; 

} 

statement x; 

 

#include<stdio.h> 

int main() 

{ 

    int x=10; 

    if (x>0) 

    x++; 

    printf("x=%d",x); 

    return 0; 

} 

 

If (text expression) 

{ 

  statement_block 1; 

} 

else 

{ 

  statement_block 2; 

} 

statement x; 

 

#include <stdio.h> 

int main()  

{ 

    int a; 

    printf("enter the value of a"); 

    scanf("%d",&a); 

    if(a%2==0) 

    printf("%d is even"); 

    else 

    printf("%d is odd"); 

    return 0; 

} 

 

1.//Write a program to find greatest of three number allow user input for giving three numbers 

#include<stdio.h> 

int main() 

{ 

    int num_1,num_2,num_3; 

    printf("enter the three numbers"); 

    scanf("%d%d%d",&num_1,&num_2,&num_3); 

    if(num_1 > num_2 && num_1 > num_3) 

    { 

        printf("num_1 is greater than num_2 and num_3"); 

    } 

    if(num_2 > num_1 && num_2 > num_3) 

    { 

        printf("num_2 is greater than num_1 and num_3"); 

    } 

    else(num_3 > num_1 && num_3 > num_2); 

    { 

        printf("num_3 is greater than num_1 and num_2"); 

    } 

    return 0; 

} 

 

If (text expression 1) 

{ 

  statement block 1; 

} 

else if (text expression 2) 

{ 

  statement block 2; 

} 

--------------------------------- 

else if( text expression N) 

{ 

  statement block N; 

} 

else  

{ 

  statement block Y; 

} 

 

switch case 

 

case 'A': 

          printf("excellent"); 

          break; 

case 'B': 

          printf("good"); 

          break; 

case 'C': 

          printf("fair"); 

          break; 

default: 

          printf("invalid grade"); 

          break; 

 

2.#include<stdio.h> 

int main() 

{ 

    int num; 

    printf("enter the number"); 

    scanf("%d",&num); 

    if(num==0) 

       printf("the value is equal to zero"); 

       else if(num>0) 

       printf("the number is positive"); 

       else 

       printf("the number is negative"); 

       return 0; 

} 

 

3.#include<stdio.h> 

int main() 

{ 

    int day; 

    printf("enter any number from 1 to 7"); 

    scanf("%d",&day); 

    switch(day) 

{ 

case 1:  

       printf("SUNDAY");  

       break; 

case 2 :  

       printf("MONDAY");  

       break; 

case 3 :  

       printf("TUESDAY");  

       break; 

case 4 :  

       printf("WEDNESDAY");  

           break; 

case 5 :  

       printf("THURSDAY");  

       break; 

case 6 :  

       printf("FRIDAY");  

       break; 

case 7 :  

       printf("SATURDAY");  

       break; 

default:  

       printf("Wrong Number"); 

} 

return 0; 

} 

 

While(condition) 

{ 

  statement_bock; 

} 

statement x; 

 

4.#include<stdio.h> 

int main() 

{ 

int i = 0; 

while(i<=10) 

{ 

printf(“%d”, i); 

i = i + 1; 

} 

return 0; 

} 

 

5.//write a c program to calculate sum of first 10 numbers from 1 to 10 

#include<stdio.h> 

int main() 

{ 

int i = 1,sum=0; 

while(i<=10) 

{ 

sum=sum + i; 

i=i+1; 

printf("sum is %d",sum); 

} 

return 0; 

} 

 

6.//if cost prize and selling prize of an item input through the keyboard.write a program weather the seller made a profit or incurd.also determine how much profit is made and incurd 

#include<stdio.h> 

int main() 

{ 

    int cost_prize; 

    int selling_prize; 

    printf("\nenter the cost_prize\n"); 

    scanf("%d",&cost_prize); 

    printf("\nenter the selling_prize\n"); 

    scanf("%d",&selling_prize); 

    if(selling_prize > cost_prize) 

    { 

        printf("seller made loss is %d\n",(selling_prize - cost_prize)); 

    } 

    else if(cost_prize > selling_prize) 

    { 

        printf("seller made profit is %d\n",(cost_prize - selling_prize)); 

    } 

    return 0; 

} 

 

for loop 

for (initialization; condition; increment/decrement/update) 

{ 

   statement block; 

} 

Statement Y; 

  

7.#include<stdio.h> 

int main() 

{ 

    int i, n; 

    printf("enter the value of n"); 

scanf("%d",&n); 

for(i=0; i<= n; i++) 

printf("%d",i); 

return 0; 

} 

 

do while loop 

Statement x; 

do 

{ 

statement_block; 

} while (condition); 

statement y; 

 

8.#include<stdio.h> 

int main() 

{ 

    int i=0; 

    do 

    { 

        printf("%d",i); 

        i=i+1; 

    } 

    while(i<=10); 

    return 0; 

} 

 

9.//write a c program to calculate root of quadratic equation 

#include <stdio.h> 

#include <math.h> 

void calculateRoots(float a, float b, float c) { 

    float discriminant, root1, root2, realPart, imaginaryPart; 

    discriminant = b * b - 4 * a * c; 

    if (discriminant > 0) { 

        root1 = (-b + sqrt(discriminant)) / (2 * a); 

        root2 = (-b - sqrt(discriminant)) / (2 * a); 

        printf("Roots are real and different.\n"); 

        printf("Root 1 = %.2f\n", root1); 

        printf("Root 2 = %.2f\n", root2); 

    } 

    else if (discriminant == 0) { 

        root1 = -b / (2 * a); 

        printf("Roots are real and the same.\n"); 

        printf("Root 1 = Root 2 = %.2f\n", root1); 

    } 

    else { 

        realPart = -b / (2 * a); 

        imaginaryPart = sqrt(-discriminant) / (2 * a); 

        printf("Roots are complex and different.\n"); 

        printf("Root 1 = %.2f + %.2fi\n", realPart, imaginaryPart); 

        printf("Root 2 = %.2f - %.2fi\n", realPart, imaginaryPart); 

    } 

} 

 

int main() { 

    float a, b, c; 

    printf("Enter coefficients a, b, and c: "); 

    scanf("%f %f %f", &a, &b, &c); 

    calculateRoots(a, b, c); 

    return 0; 

} 

 

10.//write a c program to calculate the income tax. 

if income less than 150000 no tax 

if taxable income is in range 150000 to 300000 intrest 10% 

if taxable income is in range 300000 to 500000 intrest 20% 

if taxable income is above 500000 intrest 30% 

#include <stdio.h> 

int main() { 

    float income, tax = 0.0; 

    printf("Enter your annual income: "); 

    scanf("%f", &income); 

    if (income <= 150000) { 

        tax = 0.0; 

    } else if (income <= 300000) { 

        tax = (income - 150000) * 0.10; 

    } else if (income <= 500000) { 

        tax = (300000 - 150000) * 0.10 + (income - 300000) * 0.20; 

    } else { 

        tax = (300000 - 150000) * 0.10 + (500000 - 300000) * 0.20 + (income - 500000) * 0.30; 

    } 

    printf("Your income tax is: %.2f\n", tax); 

    return 0; 

} 

 

11.//wirte a c program to calculate 20 horizontal astric using while loop 

#include <stdio.h> 

int main()  

{ 

    int i = 0;  

    while (i < 20) { 

        printf("*"); 

        i++; r 

    } 

    printf("\n");   

    return 0; 

} 

 

DAY - 4 

 

return_data_type function_name(data_type variable1, data_type variable2,..) 

{ 

    …………. 

    statements 

    …………. 

    return( variable); 

} 

 

1.#include<stdio.h> 

int sum(int a,int b); 

int main() 

{ 

    int num1,num2,total=0; 

    printf("enter the num1"); 

    scanf("%d",&num1); 

    printf("enter the num2"); 

    scanf("%d",&num2); 

    total=sum(num1,num2); 

    printf("total=%d",total); 

    return 0; 

} 

int sum(int a,int b) 

{ 

    return (a + b); 

} 

 

//call by value 

2.#include<stdio.h> 

void add(int n); 

int main() 

{ 

    int num=2; 

    printf("the value of num before calling funtion=%d",num); 

    add(num); 

    printf("the value of num after calling funtion=%d",num); 

    return 0; 

} 

void add(int n) 

{ 

    n=n+10; 

    printf("the value of called function = %d"); 

} 

 

3.#include<stdio.h> 

void add(int n); 

int main() 

{ 

    int num=2; 

    printf("\n the value of num before calling funtion=%d",num); 

    add(&num); 

    printf("\n the value of num after calling funtion=%d\n",num); 

    return 0; 

} 

void add(int n) 

{ 

    n = n + 10; 

    printf("\n the value of num in the  called function = %d",n); 

} 

 

4.//write a program to find the biggest of three interger using function 

#include <stdio.h> 

int findLargest(int a, int b, int c)  

{ 

    int largest = a;  

    if (b > largest)  

    { 

        largest = b; 

    } 

 

    if (c > largest)  

    { 

        largest = c; 

    } 

    return largest; 

} 

int main()  

{ 

    int num1, num2, num3; 

    printf("Enter three integers:\n"); 

    printf("Enter the first number: "); 

    scanf("%d", &num1); 

    printf("Enter the second number: "); 

    scanf("%d", &num2); 

    printf("Enter the third number: "); 

    scanf("%d", &num3); 

    int largest = findLargest(num1, num2, num3); 

    printf("The largest number among %d, %d, and %d is %d\n", num1, num2, num3, largest); 

    return 0; 

} 

 

5.//write a c program to calculate area of circle using function 

#include <stdio.h> 

#define PI 3.14159 

double calculateArea(double radius) 

{ 

    return PI * radius * radius; 

} 

 

int main()  

{ 

    double radius, area; 

    printf("Enter the radius of the circle: "); 

    scanf("%lf", &radius); 

    area = calculateArea(radius); 

    printf("The area of the circle with radius %.2lf is %.2lf\n", radius, area); 

    return 0; 

} 

 

6.//write a c program to calculate the sum of numbers from m to n 

#include <stdio.h> 

int calculateSum(int m, int n)  

{ 

    int sum = 0; 

    for(int i = m; i <= n; i++)  

    { 

        sum += i; 

    } 

    return sum; 

} 

 

int main()  

{ 

    int m, n, sum; 

    printf("Enter the starting value (m): "); 

    scanf("%d", &m); 

    printf("Enter the ending value (n): "); 

    scanf("%d", &n); 

    sum = calculateSum(m, n); 

    printf("The sum of numbers from %d to %d is %d\n", m, n, sum); 

    return 0; 

} 

 

7.//write a c program using a function that calculate the hypotase of right angle triangle 

#include <stdio.h> 

#include <math.h> 

double calculateHypotenuse(double side1, double side2)  

{ 

    return sqrt((side1 * side1) + (side2 * side2)); 

} 

int main()  

{ 

    double side1, side2, hypotenuse; 

    printf("Enter the length of the first side: "); 

    scanf("%lf", &side1); 

    printf("Enter the length of the second side: "); 

    scanf("%lf", &side2); 

    hypotenuse = calculateHypotenuse(side1, side2); 

    printf("The hypotenuse of the right-angled triangle with sides %.2lf and %.2lf is %.2lf\n", side1, side2, hypotenuse); 

    return 0; 

} 

 

DAY - 5 

 

1.//design a function to swap two integer varible by call by value 

#include<stdio.h> 

void swap(int a,int b) 

{ 

     int temp; 

     printf("before swap value of a=%d and b=%d",a,b); 

     temp=a; 

     a=b; 

     b=temp; 

     printf("after swap value of a=%d and b=%d",a,b); 

} 

void main() 

{ 

     int a=10; 

     int b=55; 

     swap(a,b); 

} 

 

2. //desing a function to swap two integer varible by call by reference 

#include<stdio.h> 

void swap(int a,int b) 

{ 

     int temp; 

     printf("before swap value of a=%d and b=%d",&a,&b); 

     temp=a; 

     a=b; 

     b=temp; 

     printf("after swap value of a=%d and b=%d",&a,&b); 

} 

void main() 

{ 

     int a=10; 

     int b=55; 

     swap(a,b); 

     printf("after swap value in MAIN of a=%d and b=%d",a,b); 

} 

 

3.//macro 

#include<stdio.h> 

#define PI 3.14 

int main() 

{ 

    int a,r; 

    printf("enter the radius"); 

    scanf("%d",&r); 

    a=PI*r*r; 

    printf("area is %d",a); 

    return 0; 

} 

 

4.//parameterised macro 

#include<stdio.h> 

#define SQUARE(x) ((x) * (x)) 

int main() 

{ 

    int num=4; 

    printf("square of %d is %d",num,SQUARE(num)); 

    return 0; 

}  

 

5.//Write a macro ARRAY_SIZE(arr) that calculates the number of elements in a statically allocated array. Then, use this macro to print the size of different arrays in the program. 

#include <stdio.h> 

#define ARRAY_SIZE(arr) (sizeof(arr) / sizeof((arr)[0])) 

int main()  

{ 

    int intArray[] = {1, 2, 3, 4, 5}; 

    char charArray[] = {'a', 'b', 'c', 'd', 'e', 'f'}; 

    double doubleArray[] = {1.1, 2.2, 3.3}; 

    printf("Size of intArray: %lu\n", ARRAY_SIZE(intArray)); 

    printf("Size of charArray: %lu\n", ARRAY_SIZE(charArray)); 

    printf("Size of doubleArray: %lu\n", ARRAY_SIZE(doubleArray)); 

    return 0; 

} 

 

6.//write c program to Create a macro PRINT(...) that can take a variable number of arguments and print them using printf. Your task is to write this macro and then use it to print different types and numbers of arguments. 

#include <stdio.h> 

#define PRINT(...) printf(__VA_ARGS__) 

int main()  

{ 

    int num = 42; 

    double pi = 3.14159; 

    char ch = 'A'; 

    const char *str = "Hello, World!"; 

    PRINT("This is a string: %s\n", str); 

    PRINT("This is an integer: %d\n", num); 

    PRINT("This is a double: %.5f\n", pi); 

    PRINT("This is a character: %c\n", ch); 

    PRINT("Multiple arguments: %d, %.2f, %c, %s\n", num, pi, ch, str); 

    return 0; 

} 

 

7.//write c program to String Length and Comparison Create a program that uses strlen and strcmp to: Find the length of two different strings using strlen. Compare the two strings using strcmp and print whether they are equal or not. 

#include <stdio.h> 

#include <string.h> 

int main()  

{ 

    char str1[] = "Hello, World!"; 

    char str2[] = "Hello, C Programming!"; 

    size_t len1 = strlen(str1); 

    printf("Length of str1: %zu\n", len1); 

    size_t len2 = strlen(str2); 

    printf("Length of str2: %zu\n", len2); 

    int result = strcmp(str1, str2); 

    if (result == 0) { 

        printf("The strings are equal.\n"); 

    } else { 

        printf("The strings are not equal.\n"); 

    } 

    return 0; 

} 

 

8.//Write a c program that demonstrates the use of strcpy and strcat functions. The program should: Copy one string to another using strcpy. Concatenate two strings using strcat. Print the results before and after concatenation. 

#include <stdio.h> 

#include <string.h> 

int main()  

{ 

    char source1[] = "Hello, "; 

    char source2[] = "World!"; 

    char destination[50]; 

    strcpy(destination, source1); 

    printf("After strcpy, destination: %s\n", destination); 

    strcat(destination, source2); 

    printf("After strcat, destination: %s\n", destination); 

    return 0; 

} 

 

9.//printing pattern 

#include<stdio.h> 

int main() 

{ 

    int i,j,rows; 

    printf("enter the value of rows"); 

    scanf("%d",&rows); 

    for(i=1;i<=rows;++i){ 

    for(j=1;j<=i;++j){ 

        printf("*"); 

    } 

    printf("\n"); 

    } 

    return 0; 

} 

 

10.//printing pattern 

#include<stdio.h> 

int main() 

{ 

    int i,j,rows; 

    printf("enter the value of rows"); 

    scanf("%d",&rows); 

    for(i=1;i<=rows;++i){ 

    for(j=1;j<=i;++j){ 

        printf("%d",j); 

    } 

    printf("\n"); 

    } 

    return 0; 

} 

 

11.#include<stdio.h> 

int main() 

{ 

    int i,j; 

    char input,alphabet='A'; 

    printf("enter an uppercase character you want to print in the last row"); 

    scanf("%c",&input); 

    for(i=1;i<=(input-'A'+1);++i){ 

    for(j=i;j<=i;++j){ 

        printf("%c",alphabet); 

    } 

        ++alphabet; 

        printf("\n"); 

    } 

    return 0; 

} 

 

12.#include <stdio.h> 

int main() { 

    int i, j, space, rows; 

    char input, alphabet = 'A'; 

    printf("Enter the uppercase character you want to end with: "); 

    scanf("%c", &input); 

    rows = input - 'A' + 1; 

    for (i = 1; i <= rows; ++i) { 

        for (space = 1; space <= rows - i; ++space) { 

            printf("  "); 

        } 

        for (j = 0; j != 2 * i - 1; ++j) { 

            printf("%c ", alphabet + j); 

        } 

        printf("\n"); 

    } 

 return 0; 

} 

 

13.#include <stdio.h> 

int main()  

{ 

    int i, j, space, rows; 

    char input, number = '1'; 

    printf("Enter the rows "); 

    scanf("%c", &input); 

    rows = input - '1' + 1; 

    for (i = 1; i <= rows; ++i) { 

        for (space = 1; space <= rows - i; ++space) { 

            printf("  "); 

        } 

        for (j = 0; j != 2 * i - 1; ++j) { 

            printf("%c ", number+ j); 

        } 

        printf("\n"); 

    } 

 return 0; 

} 

 

14.//Print fibanocci series 

#include <stdio.h> 

int main()  

{ 

  int t1 = 0, t2 = 1, nextTerm = 0, n; 

  printf("Enter a positive number: "); 

  scanf("%d", &n); 

  printf("Fibonacci Series: %d, %d, ", t1, t2); 

  nextTerm = t1 + t2; 

  while (nextTerm <= n)  

  { 

    printf("%d,", nextTerm); 

    t1 = t2; 

    t2 = nextTerm; 

    nextTerm = t1 + t2; 

  } 

return 0; 

} 

 

DAY - 6 

 

1.//factorial recursion 

#include<stdio.h> 

int fact(int n) 

{ 

    if(n==1) 

    return 1; 

    return(n*fact(n-1)); 

} 

int main() 

{ 

    int num; 

    scanf("%d",&num); 

    printf("factorial of %d=%d",num,fact(num)); 

    return 0; 

} 

 

2.//fibonacci series 

#include<stdio.h> 

int fibonacci(int num); 

int main() 

{  

    int i,n; 

    printf("enter the no of terms in series"); 

    scanf("%d",&n); 

    for(i=0;i<n;i++) 

    printf("fibonacci (%d)=%d",i,fibonacci(i)); 

} 

int fibonacci(int num) 

{ 

    if(num<=2) 

    return 1; 

    return (fibonacci(num -1) + fibonacci(num -2)); 

} 

 

3.#include<stdio.h> 

int sum(int n); 

int main() 

{ 

    int number,result; 

    printf("enter a positive integer"); 

    scanf("%d",&number); 

    result=sum(number); 

    printf("sum=%d",result); 

    return 0; 

} 

int sum(int n) 

{ 

    return n*(n+1)/2; 

} 

 

4.//calculate sum of digits of 5 digit number using recursion function 

#include <stdio.h> 

int sumOfDigits(int n)  

{ 

    if (n == 0)  

    { 

        return 0; 

    } else  

    { 

        return (n % 10) + sumOfDigits(n / 10); 

    } 

} 

 

int main()  

{ 

    int number, result; 

    printf("Enter a 5-digit number: "); 

    scanf("%d", &number); 

    result = sumOfDigits(number); 

    printf("The sum of the digits of %d is %d\n", number, result); 

    return 0; 

} 

 

5.//write a  c program to calcutate gcd using recursion function 

#include <stdio.h> 

int gcd(int a, int b)  

{ 

    if (b == 0)  

    { 

        return a; 

    } else  

    { 

        return gcd(b, a % b); 

    } 

} 

int main()  

{ 

    int num1, num2, result; 

    printf("Enter two integers: "); 

    scanf("%d %d", &num1, &num2); 

    result = gcd(num1, num2); 

    printf("The GCD of %d and %d is %d\n", num1, num2, result); 

    return 0; 

} 

 

6.//write a c program to reverse a number 

#include<stdio.h> 

int main() 

{ 

    int n,reverse=0,remainder,original; 

    printf("enter a integer"); 

    scanf("%d",&n); 

    original=n; 

    while(n!=0) 

    { 

        remainder=n%10; 

        reverse=reverse*10+remainder; 

        n/=10; 

    } 

    if(original%10==0){ 

        printf("reverse number=%d",reverse); 

        while(original%10==0) 

        { 

            printf("0"); 

            original/=10; 

        } 

    }else{ 

        printf("reverse number=%d",reverse); 

    } 

    return 0; 

} 

 

7.//write a c program to sum of integers to be added unit inputs 0 

#include <stdio.h> 

int main()  

{ 

    int num, sum = 0; 

    printf("Enter integers to sum (0 to stop)"); 

    while(1)  

    { 

        scanf("%d", &num); 

        if(num == 0) 

            break; 

        sum += num; 

    } 

    printf("The sum is: %d\n", sum); 

    return 0; 

} 

 

8.//write a c program to print the sum of odd integer 

#include<stdio.h> 

void main() 

{ 

    int n,i,sum=0; 

    printf("input number of terms"); 

    scanf("%d",&n); 

    printf("the odd number are"); 

    for(i=1;i<=n;i++) 

    { 

        printf("%d",2*i-1); 

        sum+=2*i-1; 

    } 

} 

 

9.//write a c program to display the largest of 5 numbers using ternary operator using do while 

#include <stdio.h> 

int main()  

{ 

    int i = 0; 

    int num, largest; 

    largest = -1000000;   

    do { 

        printf("Enter number %d: ", i + 1); 

        scanf("%d", &num); 

        largest = (num > largest) ? num : largest; 

        i++; 

    } while (i < 5); 

    printf("The largest number is: %d\n", largest); 

    return 0; 

} 

 

10.//write a c program to read the number until -1 encountered also count negative,positive,zero enter by the user using do while 

#include <stdio.h> 

int main()  

{ 

    int number; 

    int positiveCount = 0, negativeCount = 0, zeroCount = 0; 

    do { 

        printf("Enter a number (-1 to end): "); 

        scanf("%d", &number); 

        if (number > 0)  

        { 

            positiveCount++; 

        }  

        else if (number < 0 && number != -1) 

        { 

            negativeCount++; 

        }  

        else if (number == 0)  

        { 

            zeroCount++; 

        } 

    } while (number != -1); 

    printf("Positive numbers: %d\n", positiveCount); 

    printf("Negative numbers: %d\n", negativeCount); 

    printf("Zeros: %d\n", zeroCount); 

    return 0; 

} 

 

11.//write a c program to calculate average of first n number using do while loop 

#include <stdio.h> 

int main()  

{ 

    int n, i = 1; 

    float sum = 0.0, average; 

    printf("Enter the value of n: "); 

    scanf("%d", &n); 

    if (n <= 0) { 

        printf("Please enter a positive integer.\n"); 

        return 1; 

    } 

    do { 

        sum += i; 

        i++; 

    } while (i <= n); 

    average = sum / n; 

    printf("The average of the first %d numbers is: %.2f\n", n, average); 

    return 0; 

} 

 

12.//write a c program using do while loop to display square and cube of first n natural numbers 

#include <stdio.h> 

int main()  

{ 

    int n, i = 1; 

    printf("Enter the value of n: "); 

    scanf("%d", &n); 

    if (n <= 0) { 

        printf("Please enter a positive integer.\n"); 

        return 1; 

    } 

    printf("Number\tSquare\tCube\n"); 

    do { 

        printf("%d\t%d\t%d\n", i, i * i, i * i * i); 

        i++; 

    } while (i <= n); 

    return 0; 

} 

 

13.//write a c program to determine weather the given number is a palindrome or not 

#include <stdio.h> 

int main()  

{ 

    int number, originalNumber, reversedNumber = 0, remainder; 

    printf("Enter an integer: "); 

    scanf("%d", &number); 

    originalNumber = number; 

    while (number != 0)  

    { 

        remainder = number % 10; 

        reversedNumber = reversedNumber * 10 + remainder; 

        number /= 10; 

    } 

    if (originalNumber == reversedNumber)  

    { 

        printf("%d is a palindrome.\n", originalNumber); 

    } else  

    { 

        printf("%d is not a palindrome.\n", originalNumber); 

    } 

    return 0; 

} 

 

14.//if lengths of three sides of triangle enterd through keyword write a c program the triangle is valid or not. If sum of two sides > than largest of three side using do while loop 

#include <stdio.h> 

int main() { 

    int side1, side2, side3; 

    int valid = 0; 

    do { 

        printf("Enter the lengths of the three sides of the triangle:\n"); 

        printf("Side 1: "); 

        scanf("%d", &side1); 

        printf("Side 2: "); 

        scanf("%d", &side2); 

        printf("Side 3: "); 

        scanf("%d", &side3); 

        if ((side1 + side2 > side3) &&  

            (side1 + side3 > side2) &&  

            (side2 + side3 > side1)) { 

            valid = 1; // The triangle is valid 

        } 

        else  

        { 

            printf("Invalid triangle. The sum of any two sides must be greater than the third side.\n"); 

        } 

        } while (!valid); 

            printf("The triangle with sides %d, %d, and %d is valid.\n", side1, side2, side3); 

    return 0; 

} 

 

DAY - 7 

 

1.#include<stdio.h> 

int main() 

{ 

    int a,b; 

    printf("%d \n",&a); 

    printf("%d \n",&b); 

    int marks[5]={34,56,78,97,45}; 

    printf("%d \n",marks[0]); 

    printf("%d \n",marks[1]); 

    printf("%d \n",marks[2]); 

    printf("%d \n",marks[3]); 

    printf("%d \n",marks[4]); 

    return 0; 

} 

 

2.#include<stdio.h> 

int main() 

{ 

    //int score[5]; 

    int score[]={10,20,30,40}; 

    for(int i=0;i<5;i++) 

    { 

        printf("%d\n",score[i]); 

    } 

    for(int i=0;i<5;i++) 

    { 

       score[2]=90; 

       printf("%d \n",score[i]); 

    } 

    return 0; 

} 

 

3.#include<stdio.h> 

int main() 

{ 

    int n,score[10]; 

    printf("enter the no of array\n"); 

    scanf("%d",&n); 

    printf("enter array element"); 

    for(int i=0;i<n;i++) 

    { 

      scanf("%d",&score[i]);   

    } 

    for(int i=0;i<n;i++) 

    { 

        printf("%d\n",score[i]); 

    } 

    return 0; 

} 

 

DAY - 8 

 

1.#include<stdio.h> 

int main() 

{ 

    char name[5]={'N','M','I','T'}; 

    printf("name is %s\n",name); 

    scanf("%c",&name); 

    return 0; 

} 

 

Syntax of string 

char *strcat(char*s1,const char*s2); 

 

Syntax of string comparision 

Int *camp(const char*s1,char*s2); 

 

Syntax of string copy 

Char *strcpy(char*s1,const char*s2); 

 

2.#include<stdio.h> 

#include<string.h> 

int main() { 

  char s1[]="beautiful big sky country"; 

  char s2[] ="how now brown cow"; 

  printf("%d\n",strlen(s1)); 

  printf("%d\n",strlen(s2+8)); 

  printf("%d\n",strcmp(s1,s2)); 

  printf("%s\n",s1+10); 

  strcpy(s1+10,s2+8); 

  printf("%s\n",s1); 

  return 0; 

} 

 

3.#include <stdio.h>  

#include <ctype.h>  

int main()  

{  

    char ch1 = ' ';  

    char ch2 = 'a';  

      if (isspace(ch1))  

        printf("Entered character is space\n");  

    else 

        printf("Entered character %c is not space", ch1);  

      if (isspace(ch2))  

        printf("Entered character is space\n");  

    else 

        printf("Entered character %c is not space\n", ch2);  

    return 0; 

} 

 

4.#include <stdio.h>  

#include <ctype.h>  

int main()  

{  

    char ch1 = ' ';  

    char ch2 = 's'; 

    char ch3='5'; 

      if (isspace(ch1))  

        printf("Entered character is space\n");  

    else 

        printf("Entered character %c is not space\n", ch1);  

      if (isalpha(ch2))  

        printf("Entered character is letter\n");  

    else 

        printf("Entered character %c is not letter\n", ch2); 

      if(isdigit(ch3)) 

      printf("Entered character is digit\n"); 

    else 

      printf("Entered character is not digit\n");  

    return 0; 

} 

 

DAY - 9 

 

1.#include <stdio.h> 

int main()  

{ 

    int v = 14; 

    int *pv; 

    pv = &v; 

    printf("%d %d\n", v, *pv); 

    printf("%p %p\n", &v, pv); 

    printf("%X %X\n", &v, pv); 

    printf("%u %u\n", &v, pv); 

    return 0; 

} 

 

2.#include <stdio.h> 

int main()  

{ 

    int a; 

    int b, c; 

    double d; 

    char ch; 

    a = 10; b = 2.5; c = 12.36; d = 1405; ch = 'P'; 

    printf("%d is stored in location %u \n", a, &a); 

    printf("%d is stored in location %u \n", b, &b); 

    printf("%d is stored in location %u \n", c, &c); 

    printf("%f is stored in location %u \n", d, &d); 

    printf("%c is stored in location %u \n", ch, &ch); 

    return 0; 

} 

 

3.#include<stdio.h> 

int main()  

{ 

 int *p, *q; 

 int a[5]= {10,20,30,40,50}; 

 p= &a[0]; 

 q=&a[3]; 

 printf("Addres  of the  p=%X and q=%X\n", p,q); 

 printf("Difference of q-p is %d\n",q-p); 

 return 0; 

} 

 

4.#include<stdio.h> 

int main() 

{ 

  float x, y, z; 

  float *px, *py, *pz; 

  px=&x, py=&y, pz=&z; 

  printf("Enter three number:"); 

  scanf("%f %f %f", px, py, pz); 

  if(*px > *py) 

  { 

    if(*px > *pz) 

      printf("Biggest = %.2f", *px); 

    else 

      printf("Biggest = %.2f", *pz); 

  } 

  else 

  { 

    if(*py > *pz) 

      printf("Biggest = %.2f", *py); 

    else 

      printf("Biggest = %.2f", *pz); 

  } 

  return 0; 

} 

 

5.#include<stdio.h> 

#include<string.h> 

int main() 

{ 

    printf("no of in int is %u\n",sizeof(int)); 

    printf("no of in char is %u\n",sizeof(char)); 

    printf("no of in float is %u\n",sizeof(float)); 

    printf("no of in double is %u\n",sizeof(double)); 

     

    printf("no of in int* is %u\n",sizeof(int*)); 

    printf("no of in char* is %u\n",sizeof(char*)); 

    printf("no of in float* is %u\n",sizeof(float*)); 

    printf("no of in double* is %u\n",sizeof(double*)); 

    return 0; 

} 

 

In general, *(p+i) gives the value of x[i] 

 

DAY - 1 

 

1.//Toggle 1st led p1.19 continuously 

 

#include<lpc17xx.h> 

 

void delay (unsigned int a); // function declaration 

 

int main() 

{ 

LPC_GPIO1 ->FIODIR = (1<<19); //set the direction as output port 

while(1) 

{ 

LPC_GPIO1 ->FIOSET = (1<<19); //set the PORT WITH HIGH VALUE 

delay(200); 

LPC_GPIO1 ->FIOCLR = (1<<19); //set the PORT WITH LOW VALUE 

delay(200); 

} 

} 

// function defined 

void delay(unsigned int a) 

{ 

int i, j; 

for(i=0;i<a;i++) 

for(j=0;j<6000;j++); 

} 

 

2.//Toggle 1st leds as increasing and decreasing order turning leds on continuously lower and upper nibbles(done) 

 

 #include<lpc17xx.h> 

 

 #define ALL_LED_PINS (0xFF << 19) 

 #define LED_SET1(X) (0x0F << X) 

 #define LED_SET2(X) (0xF0 << X) 

    void delay (unsigned int a); 

int main (void)  

{ 

LPC_GPIO1 -> FIODIR |= ALL_LED_PINS; 

    LPC_GPIO1 -> FIOCLR  = ALL_LED_PINS; 

 

while(1) 

{ 

 

 LPC_GPIO1 -> FIOSET = LED_SET1(19); 

 LPC_GPIO1 -> FIOCLR = LED_SET2(19); 

 delay(100); 

  

 LPC_GPIO1 -> FIOSET = LED_SET2(19); 

 LPC_GPIO1 -> FIOCLR = LED_SET1(19); 

 delay(100); 

 } 

 } 

      // function definition 

   void delay(unsigned int a) 

{ 

int i, j; 

for(i=0; i<a; i++) 

for(j=0; j<2000; j++); // blinking of led time varies 

} 

 

3.//Toggle 1st buzzer p0.27 continuously 

 

#include<lpc17xx.h> 

 

void delay (unsigned int a); // function declaration 

    

int main() 

{ 

LPC_GPIO1 ->FIODIR = (1<<27); //set the direction as output port 

while(1) 

{ 

LPC_GPIO1 ->FIOSET = (1<<27); //set the PORT WITH HIGH VALUE 

delay(100); 

LPC_GPIO1 ->FIOCLR = (1<<27); //set the PORT WITH LOW VALUE 

delay(100); 

} 

} 

// function defined 

void delay(unsigned int a) 

{ 

int i, j; 

for(i=0;i<a;i++) 

for(j=0;j<2000;j++); 

} 

 

4.#include<lpc17xx.h> 

void delay(unsigned int a); 

int main() 

{ 

int i, a[9]={0x81,0x42,0x24,0x18,0x18,0x24,0x42,0x81}; 

LPC_GPIO1 -> FIODIR=(0XFF<<19); 

while(1) 

{ 

for(i=0;i<=8;i++) 

{ 

LPC_GPIO1 -> FIOSET = (a[i]<<19); 

delay(200); 

LPC_GPIO1 -> FIOCLR = (a[i]<<19); 

delay(200); 

} 

} 

} 

void delay(unsigned int a) 

{ 

int i,j; 

for(i=0;i<a;i++) 

for(j=0;j<1000j++); 

} 

 

DAY - 2 

 

1.//toggle leds with switch-2 else beep buzzer with switch-1 

#include<lpc17xx.h> 

 

#define ALL_LED_PINS (0XFF<<19) 

#define SWITCH_1(X) (1<<X) 

#define SWITCH_2(X) (1<<X) 

#define BUZZER(X) (1<<X) 

 

void delay(unsigned int a); 

 

int main() 

{ 

LPC_GPIO1 -> FIODIR |= ALL_LED_PINS;//OP PORTS 

LPC_GPIO1 -> FIOCLR |= ALL_LED_PINS;//ALL THE CLR PORTS 

 

LPC_GPIO2 -> FIODIR &= ~(SWITCH_1(11));//SWITCH-1 AS A IP PORT 

LPC_GPIO2 -> FIODIR &= ~(SWITCH_2(12));//SWITCH-1 AS A IP PORT 

 

LPC_GPIO1 -> FIODIR |= ~(BUZZER(27));//SWITCH-1 AS A IP PORT 

 

while(1) 

{ 

if(((LPC_GPIO2  -> FIOPIN) & (SWITCH_2(12)))!=0) // POLLING STATEMENT 

{ 

LPC_GPIO1 -> FIOSET = (BUZZER(27)); 

delay(100); 

LPC_GPIO1 -> FIOCLR = (BUZZER(27)); 

delay(100); 

} 

else if(((LPC_GPIO2  -> FIOPIN) & (SWITCH_2(11)))!=0)  

{ 

/*LPC_GPIO_1 -> FIOSET = ALL_LED_PINS; 

delay(100); 

LPC_GPIO_1 -> FIOCLR = ALL_LED_PINS; 

delay(100);*/ 

LPC_GPIO1 -> FIOPIN ^= ALL_LED_PINS; 

} 

} 

} 

void delay(unsigned int a) 

{ 

int i,j; 

for(i=0;i<a;i++) 

for(j=0;j<2000;j++); 

} 

 

2.//header files 

#include <lpc17xx.h> 

#include <stdint.h> 

 

//define macros 

#define LCD_DATA_PINS (0XFF << 15) 

#define LCD_RS_PIN(X) (1<<X) 

#define LCD_EN_PIN(X) (1<<X) 

 

//DECLARE THE FUNCTIONS 

void lcd_config(void); 

void lcd_cmd_write(char); 

void lcd_data_write(char); 

void lcd_str_write(char *); 

void lcd_num(unsigned int num); 

void dealy(unsigned int a); 

 

int main(void) 

{ 

char letter = 'p'; 

lcd_config(); 

lcd_data_write(letter); 

delay(1000); 

} 

void lcd_config(void) 

{ 

LPC_GPIO0 ->FIODIR |= LCD_DATA_PINS;// OP PORTS 

LPC_GPIO0 ->FIODIR |= LCD_RS_PIN(10); 

LPC_GPIO0 ->FIODIR |= LCD_EN_PIN(11); 

lcd_cmd_write(0X38); 

lcd_cmd_write(0X0E); 

lcd_cmd_write(0X01); 

lcd_cmd_write(0X80); 

return; 

} 

// for sending commands 

void lcd_cmd_write(char cmd) 

{ 

LPC_GPIO0 -> FIOCLR |= LCD_DATA_PINS: 

LPC_GPIO0 -> FIOSET |= CMD << 15: 

LPC_GPIO0 -> FIOCLR |= LCD_RS_PIN(10): 

LPC_GPIO0 -> FIOCLR |= LCD_EN_PIN(11): 

delay(100); 

LPC_GPIO0 -> FIOCLR |= LCD_EN_PIN(11): 

} 

 // for sending data 

void lcd_data_write(char dat) 

{ 

LPC_GPIO0 -> FIOCLR |= LCD_DATA_PINS: 

LPC_GPIO0 -> FIOSET |= dat << 15: 

LPC_GPIO0 -> FIOSET |= LCD_RS_PIN(10): 

LPC_GPIO0 -> FIOCLR |= LCD_EN_PIN(11): 

delay(100); 

LPC_GPIO0 -> FIOCLR |= LCD_EN_PIN(11): 

} 

void lcd_str_write(char *str); 

{ 

while(*str != '\0') 

{ 

lcd_data_write(*str); 

str++; 

} 

return; 

}  

void lcd_num(unsigned int num) 

{ 

if(num) 

{ 

lcd_num(num/10); 

lcd_data_write(num%10+ 0X30); 

} 

} 

void delay(unsigned int a) 

{ 

int i,j; 

for(i=0;i<a;i++) 

for(j=0;j<a;j++); 

} 

 

3.// Header files (FOR SINGLE WORD) 

#include <lpc17xx.h> 

#include <stdint.h> 

 

//define macros 

//Macros defining 

#define LCD_DATA_PINS (0xFF<<15) 

#define LCD_RS_PIN(X) (1<<X) 

#define LCD_EN_PIN(X) (1<<X) 

#define LCD_num(X) (1<<X) 

// DECLARE THE FUNCTION 

void lcd_config (void); 

void lcd_cmd_write (char); 

void lcd_data_write (char); 

void lcd_str_write (char *); 

void lcd_num (unsigned int num); 

void delay (unsigned int a); 

 

int main(void) 

{ 

char letter = 'S'; 

char message[]="BE HAPPY :)HAPPY!"; 

lcd_config(); 

lcd_data_write(letter); 

delay(1000); 

lcd_cmd_write(0Xc0); 

lcd_str_write(message); 

//return 0; 

} 

  // definning main prg -- configuration of led 

void lcd_config(void) 

{ 

LPC_GPIO0 -> FIODIR |= LCD_DATA_PINS;// OUTPUT PORTS 

LPC_GPIO0 -> FIODIR |= LCD_RS_PIN(10); 

LPC_GPIO0 -> FIODIR |= LCD_EN_PIN(11); 

lcd_cmd_write(0x38); 

lcd_cmd_write(0x0E); 

lcd_cmd_write(0x01); 

lcd_cmd_write(0x80); 

//return; 

} 

//for sending command 

void lcd_cmd_write (char cmd) 

{ 

LPC_GPIO0 -> FIOCLR |= LCD_DATA_PINS; 

LPC_GPIO0 -> FIOSET |= cmd << 15; 

LPC_GPIO0 -> FIOCLR |= LCD_RS_PIN(10); 

LPC_GPIO0 -> FIOSET |= LCD_EN_PIN(11); 

delay(100); 

LPC_GPIO0 -> FIOCLR |= LCD_EN_PIN(11); 

return; 

} 

 

//for sending data 

void lcd_data_write (char dat) 

{ 

LPC_GPIO0 -> FIOCLR |= LCD_DATA_PINS; 

LPC_GPIO0 -> FIOSET |= dat << 15; 

LPC_GPIO0 -> FIOSET |= LCD_RS_PIN(10); 

LPC_GPIO0 -> FIOSET |= LCD_EN_PIN(11); 

delay(100); 

LPC_GPIO0 -> FIOCLR |= LCD_EN_PIN(11); 

return; 

} 

 // FOR STRING INPUT 

void lcd_str_write(char *str) 

{ 

while(*str != '\0') 

{ 

lcd_data_write(*str); 

str++; 

} 

return; 

} 

 

void lcd_num (unsigned int num) 

{ 

if (num) 

{ 

lcd_num(num/10); 

lcd_data_write(num % 10 + 0x30); 

} 

} 

 

void delay(unsigned int a) 

{ 

int i,j; 

for(i=0;i<a;i++) 

for(j=0;j<2000;j++); 

}  

 

4.// rows as ip port and cols as op port 

#include<LPC17xx.h> 

#include "lcd_fun.c" 

#define ROWS (0xF<<4) 

#define COLS (0xF<<0) 

void COL_scan(void); 

//main 

int main() 

{ 

lcd_config(); 

while(1) 

{ 

COL_scan(); 

} 

} 

void COL_scan(void) 

{ 

int val; 

LPC_GPIO2 ->FIODIR |= ROWS; //COLS AS OP PORTS 

LPC_GPIO2 ->FIODIR &= ~COLS; //ROWS AS IP PORTS 

val = LPC_GPIO2 ->FIOPIN & COLS; //check the status of switch 

val = val>>0;  

switch(val) 

{ 

case 0x0E: lcd_str_write("COL1"); 

delay(100); 

break; 

  case 0x0D: lcd_str_write("COL2"); 

delay(100); 

break; 

case 0x0B: lcd_str_write("COL3"); 

delay(100); 

break; 

case 0x07: lcd_str_write("COL4"); 

delay(100); 

break; 

} 

} 

 

5.// rows as ip port and cols as op port 2 program 

#include<LPC17xx.h> 

#include "lcd_fun.c" 

#define ROWS (0xF<<4) 

#define COLS (0xF<<0) 

 

void row_scan(void); 

void COL_scan1(void); 

void COL_scan2(void); 

void COL_scan3(void); 

void COL_scan4(void); 

//main 

int main() 

{ 

lcd_config(); 

while(1) 

{ 

row_scan(); 

} 

} 

void row_scan(void) 

{ 

int val; 

LPC_GPIO2 ->FIODIR |= COLS; //COLS AS OP PORTS 

LPC_GPIO2 ->FIODIR &= ~ROWS; //ROWS AS IP PORTS 

val = LPC_GPIO2 ->FIOPIN & ROWS; //check the status of switch 

val = val>>4;  

switch(val) 

{ 

case 0x0E: COL_scan1(); 

delay(100); 

break; 

  case 0x0D: COL_scan2(); 

delay(100); 

break; 

case 0x0B: COL_scan3(); 

delay(100); 

break; 

case 0x07: COL_scan4(); 

delay(100); 

break; 

} 

} 

void COL_scan1(void) 

{ 

int val; 

LPC_GPIO2 ->FIODIR |= ROWS; //COLS AS OP PORTS 

LPC_GPIO2 ->FIODIR &= ~COLS; //ROWS AS IP PORTS 

val = LPC_GPIO2 ->FIOPIN & COLS; //check the status of switch 

//val = val>>4;  

switch(val) 

{ 

case 0x0E: lcd_str_write("0"); 

delay(100); 

break; 

  case 0x0D:lcd_str_write("1"); 

delay(100); 

break; 

case 0x0B: lcd_str_write("2"); 

delay(100); 

break; 

case 0x07: lcd_str_write("3"); 

delay(100); 

break; 

} 

} 

void COL_scan2(void) 

{ 

int val; 

LPC_GPIO2 ->FIODIR |= ROWS; //COLS AS OP PORTS 

LPC_GPIO2 ->FIODIR &= ~COLS; //ROWS AS IP PORTS 

val = LPC_GPIO2 ->FIOPIN & COLS; //check the status of switch 

//val = val>>4;  

switch(val) 

{ 

case 0x0E: lcd_str_write("4"); 

delay(100); 

break; 

  case 0x0D:lcd_str_write("5"); 

delay(100); 

break; 

case 0x0B: lcd_str_write("6"); 

delay(100); 

break; 

case 0x07: lcd_str_write("7"); 

delay(100); 

break; 

} 

} 

void COL_scan3(void) 

{ 

int val; 

LPC_GPIO2 ->FIODIR |= ROWS; //COLS AS OP PORTS 

LPC_GPIO2 ->FIODIR &= ~COLS; //ROWS AS IP PORTS 

val = LPC_GPIO2 ->FIOPIN & COLS; //check the status of switch 

//val = val>>4;  

switch(val) 

{ 

case 0x0E: lcd_str_write("8"); 

delay(100); 

break; 

  case 0x0D:lcd_str_write("9"); 

delay(100); 

break; 

case 0x0B: lcd_str_write("apple"); 

delay(100); 

break; 

case 0x07: lcd_str_write("B"); 

delay(100); 

break; 

} 

} 

 void COL_scan4(void) 

{ 

int val; 

LPC_GPIO2 ->FIODIR |= ROWS; //COLS AS OP PORTS 

LPC_GPIO2 ->FIODIR &= ~COLS; //ROWS AS IP PORTS 

val = LPC_GPIO2 ->FIOPIN & COLS; //check the status of switch 

//val = val>>4;  

switch(val) 

{ 

case 0x0E: lcd_str_write("C"); 

delay(100); 

break; 

  case 0x0D:lcd_str_write("D"); 

delay(100); 

break; 

case 0x0B: lcd_str_write("E"); 

delay(100); 

break; 

case 0x07: lcd_str_write("F"); 

delay(100); 

break; 

} 

} 

 

6.//ADC_POTENTIOMETER 

//#include <lpc17XX.h> 

#include <stdio.h> 

#include "lcd_fun.c" 

 

#define VREF 3.3  //REFERENCE VOLTAGE @VREFP PIN, VREFN=0 

#define ADC_CLK_EN() (1<<12)  // POWER ENABLE FOR ADC 

#define SEL_AD0_1 (1<<1)  //SEL CHANNEL AD0.1 

#define CLKDIV (3<<8) // ADC CLKDIV (ADC_CLK=PCLK/CLKDIV+1)=1MHZ 

#define PWRUP (1<<21) // SETTING TO OPERATION MODE 

#define START_CNV (1<<24)  // 001 FOR START CONVERSION 

#define ADC_DONE (1U<<31) // DEFINE IT AS UNSIGNED VALUE 

 

int main(void) 

{ 

int result=0; 

float volts=0; 

char svolts[20]; 

 

LPC_PINCON -> PINSEL1 |= (1<<16);//SELECT AD0.1 FOR PO.24 

LPC_SC -> PCONP |= ADC_CLK_EN(); // ENABLE ADC CLOCK SC=SYSTEM CLOCK 

LPC_ADC -> ADCR = PWRUP | CLKDIV | SEL_AD0_1; 

 

lcd_config(); 

 

while(1) 

{ 

LPC_ADC -> ADCR |= START_CNV;// START NEW CONVERSION 

while((LPC_ADC -> ADDR1 & ADC_DONE) ==0){} //WAIT UNTIL CONVERSION IS FINISHED 

result = (LPC_ADC -> ADDR1 >> 4) & 0XFFF; //12 BIT MASK TO EXTRACT RESULT 

 

volts = (result *VREF)/4096.0;// CONVERT RESULT TO VOLTAGE 

sprintf(svolts, "voltage=%.2f v",volts); 

lcd_str_write(svolts); 

delay(500); //slowing down to 2 conversion per second 

lcd_cmd_write(0X01); 

} 

} 

 

7.//ADC_TEMPERATURE 

//#include <lpc17XX.h> 

#include <stdio.h> 

#include "lcd_fun.c" 

 

#define VREF 3.3  //REFERENCE VOLTAGE @VREFP PIN, VREFN=0 

#define ADC_CLK_EN() (1<<12)  // POWER ENABLE FOR ADC 

#define SEL_AD0_2 (1<<2)  //SEL CHANNEL AD0.1 

#define CLKDIV (3<<8) // ADC CLKDIV (ADC_CLK=PCLK/CLKDIV+1)=1MHZ 

#define PWRUP (1<<21) // SETTING TO OPERATION MODE 

#define START_CNV (1<<24)  // 001 FOR START CONVERSION 

#define ADC_DONE (1U<<31) // DEFINE IT AS UNSIGNED VALUE 

#define T_COEFF 100.0f 

 

int main(void) 

{ 

int result=0; 

float volts=0; 

char svolts[20]; 

 

float temp=0; 

char stemp[20]; 

 

LPC_PINCON -> PINSEL1 |= (1<<18);//SELECT AD0.2 FOR PO.25 

LPC_SC -> PCONP |= ADC_CLK_EN(); // ENABLE ADC CLOCK SC=SYSTEM CLOCK 

LPC_ADC -> ADCR = PWRUP | CLKDIV | SEL_AD0_2; 

 

lcd_config(); 

 

while(1) 

{ 

LPC_ADC -> ADCR |= START_CNV;// START NEW CONVERSION 

while((LPC_ADC -> ADDR2 & ADC_DONE) ==0){} //WAIT UNTIL CONVERSION IS FINISHED 

result = (LPC_ADC -> ADDR2 >> 4) & 0XFFF; //12 BIT MASK TO EXTRACT RESULT 

 

volts = (result *VREF)/4096.0;// CONVERT RESULT TO VOLTAGE 

sprintf(svolts, "voltage=%.2f v",volts); 

lcd_str_write(svolts); 

lcd_cmd_write(0Xc0); 

 

temp=volts*T_COEFF; 

sprintf(stemp, "temp=%.2f 'c",temp); 

lcd_str_write(stemp); 

delay(500); 

lcd_cmd_write(0x01); 

} 

} 

 

8.#include<lpc17xx.h> 

#define LED_PIN(X) (1<<X) 

void TOMRdelay (unsigned int );  

 

int main() 

{ 

LPC_GPIO1 ->FIODIR |= LED_PIN(19);  

TOMRdelay(5000000); 

 

while(1) 

{ 

if(LPC_TIM0 -> IR & (1<<0)) 

{ 

LPC_GPIO1 -> FIOPIN ^= LED_PIN(19); 

LPC_TIM0 -> IR  = (1<<0); 

} 

} 

}  

void TOMRdelay(unsigned int us) 

{ 

LPC_SC -> PCONP |= (1<<1); // TIMER0 POWER CONTORL ENABLE 

LPC_SC -> PCLKSEL0 |= (0X00<<2); 

 

LPC_TIM0 -> MR0 = 1000000;//LOAD COUNT VALUE TO MR0 

LPC_TIM0 -> MCR |= (1<<0) | (1<<1); // ON COUNT REACHING MATCH VALUE RAISE AN INT 

LPC_TIM0 -> TCR = (1<<1); // INITIALIZE PC AND TC TO ZERO SIMULTANIOUSLY 

LPC_TIM0 -> TCR = (1<<0); // START TIMER COUNTER 

} 

 

9.#include<lpc17xx.h> 

#define LED_PIN(X) (1<<X) 

 

void TOMRdelay (unsigned int );  

 

int main() 

{ 

LPC_GPIO1 -> FIODIR |= LED_PIN(19); 

LPC_GPIO1 -> FIODIR |= LED_PIN(20); 

LPC_GPIO1 -> FIODIR |= LED_PIN(21); 

LPC_GPIO1 -> FIODIR |= LED_PIN(22); 

TOMRdelay(5000000); 

 

while(1) 

{ 

if(LPC_TIM0 -> IR & (1<<0)) 

{ 

LPC_GPIO1 -> FIOPIN ^= LED_PIN(19); 

LPC_TIM0 -> IR  = (1<<0); 

} 

if(LPC_TIM0 -> IR & (1<<1)) 

{ 

LPC_GPIO1 -> FIOPIN ^= LED_PIN(20); 

LPC_TIM0 -> IR  = 1<<1; 

} 

if(LPC_TIM0 -> IR & (1<<2)) 

{ 

LPC_GPIO1 -> FIOPIN ^= LED_PIN(21); 

LPC_TIM0 -> IR  = 1<<2; 

} 

if(LPC_TIM0 -> IR & (1<<3)) 

{ 

LPC_GPIO1 -> FIOPIN ^= LED_PIN(22); 

LPC_TIM0 -> IR  = 1<<3; 

} 

} 

}  

void TOMRdelay(unsigned int us) 

{ 

LPC_SC -> PCONP |= (1<<1); // TIMER0 POWER CONTORL ENABLE 

LPC_SC -> PCLKSEL0 |= (0X00<<2); 

 

LPC_TIM0 -> MR0 = 1000000;  

LPC_TIM0 -> MR1 = 3000000; 

LPC_TIM0 -> MR2 = 5000000; 

LPC_TIM0 -> MR3 = 8000000; //LOAD COUNT VALUE TO MR1 

 

LPC_TIM0 -> MCR |= (1<<0); // ON COUNT REACHING MATCH VALUE RAISE AN INT 

LPC_TIM0 -> MCR |= (1<<3); // ON COUNT REACHING MATCH VALUE RAISE AN INT 

LPC_TIM0 -> MCR |= (1<<6);  

LPC_TIM0 -> MCR |= (1<<10) | (1<<9); // INITIALIZE PC AND TC TO ZERO SIMULTANIOUSLY 

LPC_TIM0 -> TCR = (1<<0); // START TIMER COUNTER 

} 

 

10.toggle switch for 1 sec and buzzer for 2 sec 

#include<lpc17xx.h> 

#define LED_PIN(X) (1<<X) 

 

void TOMRdelay (unsigned int );  

 

int main() 

{ 

LPC_GPIO1 -> FIODIR |= LED_PIN(19); 

LPC_GPIO1 -> FIODIR |= LED_PIN(27); 

TOMRdelay(5000000); 

 

while(1) 

{ 

if(LPC_TIM0 -> IR & (1<<0)) 

{ 

LPC_GPIO1 -> FIOPIN ^= LED_PIN(19); 

LPC_GPIO1 -> FIOPIN ^= LED_PIN(27); 

LPC_TIM0 -> IR  = (1<<0); 

} 

} 

}  

void TOMRdelay(unsigned int us) 

{ 

LPC_SC -> PCONP |= (1<<1); // TIMER0 POWER CONTORL ENABLE 

LPC_SC -> PCLKSEL0 |= (0X00<<2); 

 

LPC_TIM0 -> MR0 = 1000000;  

LPC_TIM0 -> MR1 = 3000000; //LOAD COUNT VALUE TO MR1 

 

LPC_TIM0 -> MCR |= (1<<0); 

LPC_TIM0 -> MCR |= (1<<0) | (1<<1); // ON COUNT REACHING MATCH VALUE RAISE AN INT 

LPC_TIM0 -> TCR = (1<<1); // INITIALIZE PC AND TC TO ZERO SIMULTANIOUSLY 

LPC_TIM0 -> TCR = (1<<0); // ON COUNT REACHING MATCH VALUE RAISE AN INT 

} 

 

11.RTC(real time clock) 

#include <LPC17XX.h> 

#include <stdio.h> 

#include "lcd_fun.c" 

 

//PERIPHERAL CLOCK FOR RTC IS FIXED AT CCLK/8 

int main() 

{ 

char stime[20]; 

char sdate[20]; 

 

LPC_SC -> PCONP |= (1<<9); 

LPC_RTC -> CIIR =0;//DISABLE ALL THE COUNTER INCREMENT INTERRUPT 

LPC_RTC -> CCR = 1; //ENABLE TIMER COUNTERS 

 

LPC_RTC -> YEAR = 2024; 

LPC_RTC -> MONTH = 9; 

LPC_RTC -> DOM = 12; 

 

LPC_RTC -> HOUR = 10; 

LPC_RTC -> MIN = 40; 

LPC_RTC -> DOM = 12; 

 

lcd_config(); 

lcd_cmd_write(0X0C); 

 

while(1) 

{ 

//READ THE CURRENT VALUE FROM RTC 

uint8_t current_sec = LPC_RTC -> SEC; 

sprintf(stime, "TIME-%02d:%02d:%2d", LPC_RTC -> HOUR, LPC_RTC -> MIN, LPC_RTC -> SEC); 

sprintf(sdate, "date-%02d:%02d:%4d", LPC_RTC -> DOM, LPC_RTC -> MONTH, LPC_RTC -> YEAR); 

lcd_str_write(stime); 

lcd_cmd_write(0XC0); 

lcd_str_write(sdate); 

delay(100); 

lcd_cmd_write(0X80); 

} 

} 

 

12.WDT(watch dog time) 

#include <LPC17XX.h> 

void delay_ms(uint32_t); 

 

int main() 

{ 

LPC_GPIO1 -> FIODIR |= (0XFF<<19); 

LPC_GPIO1 -> FIODIR |= (1<<27); 

LPC_GPIO1 -> FIOSET |= (1<<27);//TURN ON THE BUZZER 

delay_ms(1000); 

LPC_GPIO1 -> FIOCLR |= (1<<27);// TURN OF THE BUZZER 

 

LPC_WDT -> WDCLKSEL = 0x00;// SELECT THE IRC CLK SRC=4MHZ 

LPC_WDT -> WDTC = 4000000;//SET WDT VALUE FOR TIMER PERIOD =4SEC 

LPC_WDT -> WDMOD = (1<<1) | (1<<0);//OPERATE WITH WD INTERRUPT AND RESET MODE 

LPC_WDT -> WDFEED = 0xAA; 

LPC_WDT -> WDFEED = 0x55; 

   

while(1) 

{ 

LPC_GPIO1 -> FIOSET |= (0XFF << 19);//TURN ON LED 

delay_ms(100); 

LPC_GPIO1 -> FIOCLR |= (0XFF << 19);//TURN ON LED 

delay_ms(100); 

} 

} 

void delay_ms(uint32_t ms) 

{ 

uint32_t i,j; 

for(i=0;i<ms;i++) 

{ 

for(j=0;j<1250;j++); 

} 

} 

 

13.//SINGLE EDGE PWM 

#include <LPC17XX.h> 

void delay(int a) 

{ 

int i,j; 

for(i=0;i<a;i++) 

for(j=0;j<6000;j++); 

} 

int main() 

{ 

LPC_GPIO1 -> FIODIR = (0X7F<<20); 

LPC_PINCON -> PINSEL3 &= ~(1<<4);//p1,18 as pwm1 

LPC_PINCON -> PINSEL3 |= (1<<5);//P2.4 PIN AS PWM5 

LPC_SC -> PCONP |= (1<<6);//PWM1 POWER/CLK CONTROL ENABLE 

LPC_SC -> PCLKSEL0 |= (0x01<<12); 

 

LPC_PWM1 -> PR=3;//(PCLK/PR+1)=1MHZ 

LPC_PWM1 -> MR0=10000;//TOTAL TIME PERIOD OF PWM CYCLE 10000 

LPC_PWM1 -> MCR |= (1<<1);//RESET ON MR0 

LPC_PWM1 -> LER |= (1<<0);//ENABLE MR0 LATCH 

LPC_PWM1 -> PCR |= (1<<9);//PWM1 OP ENABLE 

LPC_PWM1 -> TCR |= (1<<0) | (1<<3);//ENABLE PWM TIMER AND PWM MODE 

 

while(1) 

{ 

LPC_PWM1 -> MR1=2000;//20% DUTY CYCLE 

LPC_PWM1 -> LER |= (1<<1);//ENAVBLE TO MR LATCH 

delay(200); 

LPC_PWM1 -> MR1=4000;//40% DUTY CYCLE 

LPC_PWM1 -> LER |= (1<<1);//ENAVBLE TO MR LATCH 

delay(200); 

LPC_PWM1 -> MR1=7500;//75% DUTY CYCLE 

LPC_PWM1 -> LER |= (1<<1);//ENAVBLE TO MR LATCH 

delay(200); 

LPC_PWM1 -> MR1=10000;//100% DUTY CYCLE 

LPC_PWM1 -> LER |= (1<<1);//ENAVBLE TO MR LATCH 

delay(200); 

} 

} 

 

14.//DOUBLE EDGE PWM 

#include <LPC17XX.h> 

void delay(int a) 

{ 

int i,j; 

for(i=0;i<a;i++) 

for(j=0;j<6000;j++); 

} 

int main() 

{ 

LPC_GPIO1 -> FIODIR = (0X7F<<20); 

LPC_PINCON -> PINSEL4 &= ~(0x03 <<8);//p1,18 as pwm1 

LPC_PINCON -> PINSEL4 |= (0x01<<8);//P2.4 PIN AS PWM5 

LPC_SC -> PCONP |= (1<<6);//PWM1 POWER/CLK CONTROL ENABLE 

LPC_SC -> PCLKSEL0 |= (0x01<<12); 

 

LPC_PWM1 -> PR=3;//(PCLK/PR+1)=1MHZ 

LPC_PWM1 -> MR0=10000;//TOTAL TIME PERIOD OF PWM CYCLE 10000 

LPC_PWM1 -> MCR |= (1<<1);//RESET ON MR0 

LPC_PWM1 -> LER |= (1<<0);//ENABLE MR0 LATCH 

LPC_PWM1 -> PCR |= (1<<5);//ENABLE MR0 LATCH 

LPC_PWM1 -> PCR |= (1<<13);//PWM1 OP ENABLE 

LPC_PWM1 -> TCR |= (1<<0) | (1<<3);//ENABLE PWM TIMER AND PWM MODE 

 

while(1) 

{ 

LPC_PWM1 -> MR4=2000; 

LPC_PWM1 -> MR5=3000;//20% DUTY CYCLE 

LPC_PWM1 -> LER |= (1<<5) | (1<<4);//ENAVBLE TO MR LATCH 

delay(100); 

LPC_PWM1 -> MR4=3000; 

LPC_PWM1 -> MR5=6000; 

//40% DUTY CYCLE 

LPC_PWM1 -> LER |= (1<<5) | (1<<4);//ENAVBLE TO MR LATCH 

delay(100); 

LPC_PWM1 -> MR4=2000; 

LPC_PWM1 -> MR5=9000;//75% DUTY CYCLE 

LPC_PWM1 -> LER |= (1<<5) | (1<<4);//ENAVBLE TO MR LATCH 

delay(100); 

} 

} 

 

15.INTERRUPT 

#include <LPC17XX.h> 

#include <stdint.h> 

#include "uart.h" 

 

void NVIC_config(void); 

void timer0_config(void); 

int main() 

{ 

LPC_GPIO1 -> FIODIR |=(1<<19); 

uart_config();// INITIALIZE UART CONFIGURATION 

timer0_config();//INITIALIZE TIMER0 CONFIGURATION 

NVIC_config();//INITIALIZE INTERRUPT CONFIGURATION 

 

while(1) 

{ 

LPC_GPIO1 -> FIOSET |=(1<<19);// SET P1.19 HIGH 

delay_ms(100); 

LPC_GPIO1 -> FIOCLR |= (1<<19);//SET P1.19 LOW 

delay_ms(100); 

} 

} 

void timer0_config(void); 

{ 

LPC_SC -> PCONP |= (1<<1); 

LPC_TIM0 -> PR=0; 

LPC_TIM0 -> MR0=4000000;//10 SECONDS 

LPC_TIM0 -> MCR(1<<0) | (1<<1); 

LPC_TIM0 -> TCR=1<<1;//RESET TIMER0 

LPC_TIM0 -> TCR=1<<0;//ENABLE TIMER0 

} 

void NVIC_config(void); 

{ 

NVIC_ClearPendingIRQ(TIMER0_IRQn);//clear pending interrupt for timer0 

NVIC_SetPriority(TIMER0_IRQn,1);//SET PRIORITY 

NVIC_EnableIRQ(TIMER0_IRQn);//ENABLE TIMER0 INTERRUPT 

} 

void TIMER0_IRQHandler(void) 

{ 

uart_str("Interrupt occured"); //sending a message through uart 

delay_ms(100); 

LPC_TIM0 -> IR=1<<0;//CLR INTERRUPT FLAG 

NVIC_ClearPendingIRQ(TIMER0_IRQn);//CLEAR PENDING INTERRUPT FOR TIMER0 

} 

 

16.#define UART_H 

#define UART_H 

 

#include <lpc17xx.h> 

 

//#define UART_PCONP_ENABLE   (0x00000008) 

//#define UART_LCR_SETUP      (0x00000083) 

//#define UART_LCR_WORD_LEN8  (0x00000003) 

//#define UART_FCR_ENABLE     (0x07) 

 

void uart_config(void); 

void uart_data(unsigned char d); 

void uart_str(unsigned char *ptr); 

void uart_num(unsigned int num); 

unsigned char uart_rx(void); 

void delay_ms(unsigned int a); 

 

void uart_config() 

{ 

    LPC_SC->PCONP |= 0x00000008;   // UART0 peripheral enable 

    LPC_PINCON->PINSEL0 =0x00000050; 

    LPC_UART0->LCR = 0x00000083; // Enable divisor latch,parity disable, 

                                 //1 stop bit, 8-bit word length 

    LPC_UART0->DLM = 0X00; 

    LPC_UART0->DLL = 0x1A;      // Select baud rate 9600 bps for 4Mhz 

    LPC_UART0->LCR = 0x00000003; // Disable divisor latch 

    LPC_UART0->FCR = 0X07;    // FIFO enable, RX FIFO reset, TX FIFO reset 

} 

 

void uart_data(unsigned char d) 

{ 

    while (!(LPC_UART0->LSR & (1 << 5))); // Check THR is empty or not, 

                                           //use polling method 

    LPC_UART0->THR = d;                    // Load the data to THR 

    delay_ms(10); 

} 

 

void uart_str(unsigned char *ptr) 

{ 

    while (*ptr != '\0') 

    { 

        uart_data(*ptr); 

        ptr++; 

    } 

} 

 

unsigned char uart_rx() 

{ 

    while (!(LPC_UART0->LSR & (1 << 0))); //Check RBR is received 

                                         //data or not 

    return LPC_UART0->RBR; 

} 

 

void uart_num(unsigned int num) 

{ 

    if (num) 

    { 

        uart_num(num / 10); 

        uart_data(num % 10 + 0x30); 

    } 

} 

 

void delay_ms(unsigned int a) 

{ 

    unsigned int i, j; // 100x 6000/60Mhz = 0.01s-- 

    for (i = 0; i < a; i++) 

        for (j = 0; j < 6000; j++); 

} 

 

17.//uart tx 

#include <LPC17XX.h> 

#include <stdio.h> 

 

void uart_Init(void); 

void uart_byte_transmit(char ch); 

void uart_str_transmit(char *str); 

void delay_ms(unsigned int ms); 

 

int main() 

{ 

char ch='k'; 

char str[]="EEE ROCKS"; 

uart_Init(); 

 

uart_byte_transmit(ch); 

uart_byte_transmit(0x0D); //carriage return 

uart_byte_transmit(0x0A); //line feed 

 // both 0D and 0A performs enter operation 

delay_ms(100); 

uart_str_transmit(str); 

} 

 

void uart_Init(void) 

{ 

LPC_SC -> PCONP |=(1<<3);//UNABLE UART0 

LPC_SC -> CLKSRCSEL |=(0X00); 

LPC_SC -> PCLKSEL0 &= ~((1<<7)|(1<<6)); 

 

LPC_PINCON -> PINSEL0 |= (1<<4);//P0.2 pin as uart TX pin 

LPC_PINCON -> PINSEL0 &= ~(1<<5); 

LPC_PINCON -> PINSEL0 |= (1<<6);//P0,3 pin as uart Tx pin 

LPC_PINCON -> PINSEL0 &= ~(1<<7); 

 

//no parity, 1 stop bit and 8 bit word length 

LPC_UART0 -> LCR |= (0X03); 

LPC_UART0 -> LCR |= (1<<7); // ENABLE DIVISOR LATCH 

 

LPC_UART0 -> DLM = (0X00); 

LPC_UART0 -> DLL = (0X06); 

LPC_UART0 -> FDR |= (0Xc1); 

LPC_UART0 -> FCR |= (0X07);//FIFO ENABLE 

LPC_UART0 -> LCR &= ~(1<<7);//DISABLE DIVISOR LATCH 

} 

 

void delay_ms(unsigned int ms) 

{ 

int i,j; 

for(i=0;i<ms;i++) 

for(j=0;j<6000;j++); 

} 

 

void uart_str_transmit(char *str) 

{ 

while(*str !='\0') 

{ 

uart_byte_transmit(*str); 

str++; 

} 

uart_byte_transmit(0x0D); //carriage return 

uart_byte_transmit(0x0A); //line feed 

} 

 

void uart_byte_transmit(char ch) 

{ 

while((LPC_UART0 -> LSR&(1<<5)==0)) {}//checking for thr is empty or not 

LPC_UART0 -> THR = ch; 

delay_ms(100); 

} 

 

18.// uart tx_rx 

#include <LPC17XX.h> 

#include <stdint.h> 

#include"lcd_fun.c" 

 

  

void uart_init(void); // uart initialization 

void uart_byte_transmit(char ch); 

void uart_str_transmit(char *ptr); 

char uart_byte_receive(void); 

void delay_ms(unsigned int ms); 

 

int main() 

{ 

char ch; 

uart_init(); 

lcd_config(); 

do 

{ 

 

ch = uart_byte_receive(); 

lcd_data_write(ch); 

uart_byte_transmit(ch); 

} 

while(ch !='.'); 

} 

 

 void uart_init() 

{ 

LPC_PINCON -> PINSEL0 |= 0X50; 

 

LPC_SC -> PCONP |= (1<<3); // ENABLE UART0 

LPC_SC -> CLKSRCSEL |= (0X00);  

LPC_SC -> PCLKSEL0 &= ~((1<<7)|(1<<6));  

 

 

// no parity, 1 stop bit and 8 bit word length 

 

LPC_UART0 -> LCR |= (0X03);   // OR (3<<0) 

LPC_UART0 -> LCR |= (1<<7); // ENABLE DIVISOR LATCH 

 

 LPC_UART0 -> DLM = (0X00);   

 LPC_UART0 -> DLL = (0X06); 

 

 LPC_UART0 -> FDR  |= (0Xc1); // fractional value 

 LPC_UART0 -> FCR  |= (0X07); // FUIFO ENABLE 

 LPC_UART0 -> LCR &= ~(1<<7); // DISABLE DIVISOR LATCH 

 

 } 

void uart_byte_transmit(char ch) 

{ 

while((LPC_UART0-> LSR&(1<<5)==0)){} 

LPC_UART0 -> THR = ch; 

 } 

 

void uart_str_transmit(char *ptr) 

{ 

while(*ptr != '\0') 

{ 

uart_byte_transmit(*ptr); 

ptr++; 

} 

 uart_byte_transmit(0X0D); // CARRIAGE RETURN 

 uart_byte_transmit(0X0A); // LINE FEED 

} 

 

char uart_byte_receive(void) 

{ 

char ch; 

while((LPC_UART0-> LSR&(1<<0)==0)){}// checking for the THR is empty or not 

ch = LPC_UART0 -> RBR; 

return ch ; 

} 

 

 void delay_ms(unsigned int ms) 

{ 

int i,j; 

for(i=0;i<ms;i++) 

for(j=0;j<2000;j++); 

} 

 

19.//single bite I2c transmit and receive Program 

#include <LPC17XX.h> 

#include <stdint.h> 

#include "lcd_fun.c" 

 

//function declaration 

void i2c_config(void); 

void i2c_start(void); 

void i2c_mem_write(uint8_t); 

void i2c_stop(void); 

uint8_t i2c_mem_read(uint8_t ack); 

 

int main() 

{ 

uint8_t val; 

i2c_config(); 

lcd_config(); 

 

lcd_str_write("I2C MEM WRITE.."); 

i2c_start(); 

i2c_mem_write(0XA0);//writing to EEPROM - DEVICE ADDRESS 

i2c_mem_write(0X30);//writing to EEPROM - ADDRESS LOCATION IN EEPROM 

i2c_mem_write('K');//WRITING DATA 

i2c_stop(); 

lcd_cmd_write(0Xc0);//moving cursor to 2nd line on lcd 

lcd_str_write("WRITE IS DONE.."); 

delay(2000); 

lcd_cmd_write(0X01);//clear the screen 

 

lcd_str_write("I2C MEM WRITE.."); 

i2c_start(); 

i2c_mem_write(0XA0);//writing to EEPROM - DEVICE ADDRESS 

i2c_mem_write(0X30); 

i2c_start(); 

i2c_mem_write(0XA1); //read operation 

val=i2c_mem_read(0); 

i2c_stop(); 

lcd_cmd_write(0Xc0); 

lcd_data_write(val); 

} 

void i2c_config(void) 

{ 

LPC_SC -> PCONP |= (1<<7);//ENABLE POWER TO I2C 

LPC_SC ->PCLKSEL0 |= ~((1<<15)|(1<<14));//PCLK=CCLK/4=1MHZ 

 

LPC_PINCON -> PINSEL1 |= (1<<22);//P0.27 SDA 

LPC_PINCON -> PINSEL1 &= ~(1<<23); 

LPC_PINCON -> PINSEL1 |= (1<<24);//P0.28 SCL 

LPC_PINCON -> PINSEL1 &= ~(1<<25); 

 

LPC_I2C0 -> I2SCLH =10; 

LPC_I2C0 -> I2SCLL =10;//SCLK FREQUENCY = PCLK/(10+10)=50KHZ FOR 50% DC 

LPC_I2C0 -> I2CONSET |= (1<<16);//ENABLE I2C FUNCTION 

} 

void i2c_start(void) 

{ 

LPC_I2C0 -> I2CONCLR |= (1<<3);//CLEAR I2C INT FLAG 

LPC_I2C0 -> I2CONSET |= (1<<5);//SENDING START CONDITION BIT 

while((LPC_I2C0 -> I2CONSET & (1<<3))==0) {}; 

LPC_I2C0 -> I2CONCLR |= (1<<5);//CLR AFTER WRITING HAS BEEN PERFORMED 

LPC_I2C0 -> I2CONCLR |= (1<<3);//CLR INT FLAG 

} 

void i2c_mem_write(uint8_t d) 

{ 

LPC_I2C0 -> I2DAT =d;//LOAD THE DATA ON TO THE I2C DATA REGISTER 

while((LPC_I2C0 -> I2CONSET & (1<<3))==0) {}; 

LPC_I2C0 -> I2CONCLR |= (1<<3);//CLR INT FLAG 

} 

void i2c_stop(void) 

{ 

LPC_I2C0 -> I2CONSET |= (1<<4);//SENDING STOP CONDITION BIT 

while((LPC_I2C0 -> I2CONSET & (1<<4))==1) {}// WAIT FOR STOP CONDTION 

} 

uint8_t i2c_mem_read(uint8_t ack) 

{ 

uint8_t val; 

if(ack) 

LPC_I2C0 -> I2CONSET & (1<<2);//SEND ACK 

else 

LPC_I2C0 -> I2CONSET & (1<<2);//SEND NO ACK 

while((LPC_I2C0 ->I2CONSET & (1<<3))==0) {}//check for i2c int 

val=LPC_I2C0 -> I2DAT;//LOAD READ DATA TO VARIABLE VAL 

LPC_I2C0 -> I2CONCLR |= (1<<3);//CLR INT FLAG 

return val; 

} 

 

20.//DECODE MODE 

#include <lpc17xx.h> 

#include <stdint.h> 

 

#define SS (1<<6) //SLAVE SELECT PIN 

 

void ssp_spi_config(void); 

void spi_data_write(uint16_t); 

void delay(uint32_t); 

 

int main() 

{ 

ssp_spi_config(); 

spi_data_write(0X0C01);//to make display unit operational 

spi_data_write(0X0A0F);//intensity register for max brightness 

spi_data_write(0X0B03);//scan limit register for digit 0-3 

spi_data_write(0X090F);//decode register with decode mode,first 4 displays 

 

while(1) 

{ 

spi_data_write(0X0101);//display char 1 on first disply unit(digit 0) 

spi_data_write(0X0207);//display char 7 on second disply unit(digit 1) 

spi_data_write(0X0306);//display char 6 on third disply unit(digit 2) 

spi_data_write(0X0408);//display char 8 on fourth disply unit(digit 3) 

 

delay(1000); 

 

spi_data_write(0X010C);//display char H on first disply unit(digit 0) 

spi_data_write(0X020B);//display char E on second disply unit(digit 1) 

spi_data_write(0X030D);//display char L on third disply unit(digit 2) 

spi_data_write(0X040E);//display char P on fourth disply unit(digit 3) 

 

delay(1000); 

} 

} 

 

void ssp_spi_config(void) 

{ 

LPC_SC -> PCON |= (1<<10);//ENABLE POWER TO SSP1 PERIPHERAL 

LPC_SC -> PCLKSEL0 |= (3<<20);//PCLK=CCLK/8=4MHZ/8=500KHZ 

 

LPC_PINCON -> PINSEL0 |= (1<<15);//P0,7 PIN AS SCLK 

LPC_PINCON -> PINSEL0 &= ~(1<<14);  

 

LPC_PINCON -> PINSEL0 |= (1<<17);//P0,8 PIN AS MISO 

LPC_PINCON -> PINSEL0 &= ~(1<<16); 

 

LPC_PINCON -> PINSEL0 |= (1<<19);//P0,9 PIN AS MOSI 

LPC_PINCON -> PINSEL0 &= ~(1<<18); 

 

LPC_GPIO0 -> FIODIR |= SS;//CONFIG P0.6 AS GPIO OUTPUT 

 

LPC_SSP1 -> CR0 |= 0X0B;//FOR 12 BIT TRANSFER 

LPC_SSP1 -> CR0 &= ~(0X03<<4);//SPI FORMAT 

LPC_SSP1 -> CR0 &= ~(0X03<<6);//MODE-0 OPERATION 

LPC_SSP1 -> CR0 &= ~(0XFF<<8);//SCR=00,USE FORMULA 

 

LPC_SSP1 -> CPSR |=20;//PRESCALAR CLOCK=PCLK/CPSR=500KHZ/20=25KHZ 

 

LPC_SSP1 -> CR1 &= ~(1<<0);//NORMAL MODE 

LPC_SSP1 -> CR1 |= (1<<1);//ENABLE SSP CONTROLLER 

LPC_SSP1 -> CR1 &= ~(1<<2);//MASTER MODE 

} 

void spi_data_write(uint16_t data) 

{ 

LPC_GPIO0 -> FIOCLR = SS;//CONNECT SLAVE 

while(!(LPC_SSP1 -> SR & (1<<1))) {} //WAIT IF TX FIFO IS FULL 

LPC_SSP1 -> DR = data; 

while((LPC_SSP1 -> SR & (1<<4))) {} //WAIT TILL SPI BECOMES IDEAL  

LPC_GPIO0 -> FIOSET = SS;//DISCONNECT SLAVE 

} 

void delay(uint32_t millis) 

{ 

uint32_t i,j; 

for(i=0; i<millis; i++) 

{ 

for(j=0; j<6000; j++); 

} 

} 

 

 # embedded-system
