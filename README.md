# ASSI3

**Q1.**
Code.
#include <stdio.h>

int main() {
  char character; // Declare a variable to store the input character

  // Prompt the user to enter a character
  printf("Enter a character: ");
  // Read the input character and store it in the variable character
  scanf(" %c", &character);

  // Check if the character is a letter
  if ((character >= 'A' && character <= 'Z') || (character >= 'a' && character <= 'z')) {
    // If it's a letter, print a message indicating so
    printf("The entered character is a letter. \n");
  }
  // Check if the character is a digit
  else if (character >= '0' && character <= '9') {
    // If it's a digit, print a message indicating so
    printf("The entered character is a digit. \n");
  }
  // If the character is neither a letter nor a digit
  else {
    // Print a message indicating it's a special symbol
    printf("The entered character is a special symbol.\n");
  }

  return 0; // Indicate successful completion of the program
}
Algorithm of code 1.
1 Start
2 Include the necessary header file stdio.h for standard input/output functions.
3 Define the main function:
•	Declare a character variable character to store the input character.
•	Prompt the user to enter a character.
•	Read the input character using scanf() and store it in the variable character.
•	Check if the entered character is a letter:
•	If the character is within the range of uppercase letters ('A' to 'Z') or lowercase letters ('a' to 'z'), print a message indicating that it is a letter.
•	Check if the entered character is a digit:
•	If the character is within the range of digits ('0' to '9'), print a message indicating that it is a digit.
•	If the character is neither a letter nor a digit:
4 Print a message indicating that it is a special symbol.
5 End 

**Q2.**
Code.
#include <stdio.h>

int main() {
  float hardness, carbon_content, tensile_strength;

  // Prompt user to input hardness, carbon content, and tensile strength
  printf("Enter hardness, carbon content, and tensile strength of the steel: ");
  scanf("%f %f %f", &hardness, &carbon_content, &tensile_strength);

  // Check conditions and assign grade accordingly
  if (hardness > 50 && carbon_content < 0.7 && tensile_strength > 5600)
    printf("Grade is 10\n");
  else if (hardness > 50 && carbon_content < 0.7)
    printf("Grade is 9\n");
  else if (carbon_content < 0.7 && tensile_strength > 5600)
    printf("Grade is 8\n");
  else if (hardness > 50 && tensile_strength > 5600)
    printf("Grade is 7\n");
  else if (hardness > 50 || carbon_content < 0.7 || tensile_strength > 5600)
    printf("Grade is 6\n");
  else
    printf("Grade is 5\n");

  return 0;
}

Algorithm of code 2.
1. Start
2. Declare variables `hardness`, `carbon content`, and `tensile strength` of type float.
3. Prompt the user to input hardness, carbon content, and tensile strength of the steel.
4. Read the input values and store them in the respective variables.
5. Check the conditions to determine the grade of steel.
•	If hardness > 50 AND carbon content < 0.7 AND tensile strength > 5600, then
Print Grade is 10.
•	Else if hardness > 50 AND carbon content < 0.7, then
Print Grade is 9.
•	Else if carbon content < 0.7 AND tensile strength > 5600, then
Print Grade is 8
•	Else if hardness > 50 AND tensile strength > 5600, then
 Print Grade is 7.
•	Else if hardness > 50 OR carbon content < 0.7 OR tensile strength > 5600, then Print Grade is 6.
6. Else Print Grade is 5.
7. End

**Q3**.
Code.
#include <stdio.h>

int main() {
  float sidel, side2, side3;

  // Prompt user to input the lengths of the three sides of the triangle
  printf("Enter the lengths of the three sides of the triangle: ");
  scanf("%f %f %f", &sidel, &side2, &side3);

  // Check if the triangle is equilateral (all sides are equal)
  if (sidel == side2 && side2 == side3) {
    printf("Equilateral triangle\n");
  }
  // Check if the triangle is isosceles (two sides are equal)
  else if (side1 == side2 || side1 == side3 || side2 == side3) {
    printf("Isosceles triangle\n");
  }
  // Check if the triangle is a right-angled triangle
  else if ((sidel * sidel + side2 * side2 == side3 * side3) ||
           (sidel * sidel + side3 * side3 == side2 * side2) ||
           (side2 * side2 + side3 * side3 == sidel * sidel)) {
    printf("Right-angled triangle\n");
  }
  // If the triangle is not equilateral, isosceles, or right-angled, it must be scalene
  else {
    printf("Scalene triangle\n");
  }

  return 0;
}

Algorithm for Q3 code: 
1. Start
2. Declare variables side1, side2, and side3 of type float.
3. Prompt the user to input the lengths of the three sides of the triangle.
4. Read the input values and store them in the respective variables.
5. Check if the triangle is equilateral (all sides are equal):
•	If side1 is equal to side2 AND side2 is equal to side3, then Print "Equilateral triangle".
•	Else, continue to the next step.
6.Check if the triangle is isosceles (at least two sides are equal):
7.If side1 is equal to side2 OR side1 is equal to side3 OR side2 is equal to side3, then.
  Print "Isosceles triangle".
•	Else, continue to the next step.
•	Check if the triangle is a right-angled triangle:
•	If (side1^2 + side2^2 = side3^2) OR (side1^2 + side3^2 = side2^2) OR (side2^2 + side3^2 = side1^2), then
•	Print "Right-angled triangle".
 Else, continue to the next step.
8. If the triangle is not equilateral, isosceles, or right-angled, it must be scalene:
    Print "Scalene triangle".
9. End


**Q4**.
Code.
#include <stdio.h>

int main() {
  float num1, num2, num3, max;

  // Prompt user to input three numbers
  printf("Enter three numbers: ");
  scanf("%f %f %f", &num1, &num2, &num3);

  // Use conditional operators to find the greatest number
  max = (num1 > num2) ? ((num1 > num3) ? num1 : num3) : ((num2 > num3) ? num2 : num3);

  // Print the greatest number
  printf("The greatest number is: %.2f\n", max);

  return 0;
}

Algorithm for Q4 code: 
1. Start
2. Declare variables num1`, num2, num3, and max of type float.
3. Prompt the user to input three numbers.
4. Read the input values and store them in variables `num1`, `num2`, and `num3`.
5. Use conditional operators to find the greatest number:
   1. If num1 is greater than num2, then:
    2 If num1 is also greater than num3, assign num to max.
   3 Otherwise, assign num3 to max.
    Otherwise, if num2 is greater than num3, assign num2 to max.
   Otherwise, assign num3 to max.
6. Print the value of max as the greatest number.
7. End


**Q5.**
Code.
#include <stdio.h>
#include <math.h> // Include math.h for fabs function

int main() {
  float angle1, angle2, angle3;

  // Prompt user to input three angles of the triangle
  printf("Enter the three angles of the triangle: ");
  scanf("%f %f %f", &angle1, &angle2, &angle3);

  // Check if the sum of angles is approximately equal to 180 degrees
  if (fabs(angle1 + angle2 + angle3 - 180) < 0.0001) {
    printf("A triangle can be formed with the given angles.\n");
  } else {
    printf("A triangle cannot be formed with the given angles.\n");
  }

  return 0;
}

Algorithm for Q5 code: 
1 Define a function named is Palindrome that takes an integer as input and returns 1 if the number is a palindrome, and 0 otherwise.
2 Inside the is Palindrome function:
Convert the integer to a string or array of characters.
Initialize two pointers, one pointing to the beginning of the string and the other to the end.
•	Compare the characters at these pointers. If they match, move the pointers towards each other until they meet or cross each other.
•	If all character’s match, return 1 (indicating that the number is a palindrome); otherwise, return 0.
3 In the main function:
Prompt the user to enter an integer.
Call the is Palindrome function with the user input as an argument.
Print whether the entered number is a palindrome or not.


**Q6.**
Code.
#include <stdio.h>

// Function to calculate the nth Fibonacci number recursively with memoization
int fibonacci(int n, int memo[]) {
  if (n <= 1)
    return n;
  // Check if the Fibonacci number for n has already been calculated
  if (memo[n] != -1)
    return memo[n];
  // Calculate the Fibonacci number recursively and store it in the memo array
  memo[n] = fibonacci(n - 1, memo) + fibonacci(n - 2, memo);
  return memo[n];
}

int main() {
  int memo[100] = {-1}; // Initialize the memo array with -1
  int i;
  // Calculate the first 25 Fibonacci numbers and print them
  for (i = 0; i < 25; i++) {
    printf("%d ", fibonacci(i, memo));
  }
  printf("\n");

  return 0;
}

Algorithm for Q6 code: 
1 Start
2 Include the necessary header file stdio.h for standard input and output functions.
3 Define a recursive function Fibonacci (int n, int memo []) which takes an integer n as input and returns the nth Fibonacci number. Also, it takes an array memo [] for memorization.
If n is less than or equal to 1, return n.
If the Fibonacci number for n has already been calculated (i.e., memo[n] is not equal to -1), return memo[n].
Otherwise, calculate the Fibonacci number recursively by summing up the (n-1)th and (n-2)th Fibonacci numbers, store it in memo[n], and return memo[n].
4 Define the main function.
Initialize an array memo [] of size 25 with -1, indicating that Fibonacci numbers have not been calculated yet.
Iterate i from 0 to 24.
Inside the loop, call the Fibonacci () function with the current value of i and memo [], and print the result.
5 Print a new line for formatting.
6 End.


**Q7**.
Code.
#include <stdio.h>

// Function to recursively find and print prime factors
void primeFactorsRecursive(int n, int divisor) {
    if (n <= 1)
        return;
    while (n % divisor != 0)
        divisor++;
    printf("%d ", divisor);
    primeFactorsRecursive(n / divisor, divisor);
}

int main() {
    int num;
    printf("Enter a positive integer: ");
    scanf("%d", &num);
    if (num <= 0) {
        printf("Please enter a positive integer.\n");
        return 1; // Exit with error code 1
    }
    printf("Prime factors of %d are: ", num);
    primeFactorsRecursive(num, 2);
    printf("\n");
    return 0;
}

Algorithm for Q7 code: 
1 Start
2 Include the necessary header file stdio.h for standard input and output functions.
3 Define a function prime Factors Recursive (int n, int divisor) to recursively find and print the prime factors of a positive integer n starting from a divisor divisor.
If n is less than or equal to 1, return without any action.
While n is not divisible by divisor, increment divisor by 1.
Print the current divisor.
Recursively call prime Factors Recursive () with n divided by divisor as the new n and divisor unchanged.
4 Define the main function.
Prompt the user to enter a positive integer and store it in the variable num.
If num is less than or equal to 0, print an error message and exit with error code 1.
Print a message indicating that prime factors are being calculated for num.
Call the prime Factors Recursive () function with num as the input and 2 as the initial divisor.
Print a new line for formatting.
5 End.


**Q8.**
Code.
#include <stdio.h>

// Function to recursively find and display the binary equivalent of a decimal integer
void decimalToBinary(int n) {
    // Base case: If the decimal number is greater than 1, continue recursion
    if (n > 1)
        decimalToBinary(n / 2); // Recursively call decimalToBinary with the integer division of n by 2
    printf("%d", n % 2); // Print the remainder of n divided by 2, which gives the binary digit
}

int main() {
    int decimalNum;
    printf("Enter a decimal integer: ");
    scanf("%d", &decimalNum);

    // Check if the entered decimal number is non-negative
    if (decimalNum < 0) {
        printf("Please enter a non-negative integer. \n");
        return 1; // Exit with error code 1 indicating an error
    }

    printf("Binary equivalent: ");
    if (decimalNum == 0)
        printf("0"); // If the decimal number is 0, print its binary equivalent as directly
    else
        decimalToBinary(decimalNum); // Call the decimalToBinary function to find and display the binary equivalent

    printf("\n");
    return 0;
}

Algorithm for Q8 code: 
1 Start
2 Include the necessary header file stdio.h for standard input and output functions.
3 Define a recursive function decimal To Binary(int n) to find and display the binary equivalent of a decimal integer n.
•	If n is greater than 1, recursively call decimal ToBinary() with n divided by 2.
•	Print the remainder of n divided by 2, which represents the binary digit.
•	4 Define the main function.
•	Prompt the user to enter a decimal integer and store it in the variable decimal Num.
•	If decimalNum is less than 0, print an error message and exit with error code 1.
•	Print "Binary equivalent: ".
•	If decimal Num is 0, print its binary equivalent as "0".
•	Otherwise, call the decimal To Binary() function with decimal Num as input to find and display its binary equivalent.
Print a new line for formatting.
5 End.


**Q9.**
Code.
#include <stdio.h>

// Function to perform circular shifting of three variables
void circularShift(int *a, int *b, int *c) {
    int temp = *a;
    *a = *b;
    *b = *c;
    *c = temp;
}

int main()
{
    // Initialize variables
    int x = 5, y = 8, z = 10;

    // Perform circular shift
    circularShift(&x, &y, &z);

    // Print results
    printf("After circular shift: x=%d, y=%d, z=%d\n", x, y, z);

    return 0;
}

Algorithm for Q9 code: 
1 Start
2 Include the necessary header file stdio.h for standard input and output functions.
3 Define a function circularShift(int *a, int *b, int *c) to perform circular shifting of three variables.
•	Take pointers to three integer variables a, b, and c as arguments.
•	Store the value of c in a temporary variable temp.
•	Assign the value of b to c.
•	Assign the value of a to b.
•	Assign the stored value of c (in temp) to a.
4 Define the main function.
•	Initialize three integer variables x, y, and z with values 5, 8, and 10, respectively.
•	Call the circularShift() function with pointers to x, y, and z to perform circular shifting.
•	Print the values of x, y, and z after the circular shift.
5 End.


**Q10**.
Code.
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char line[100]; // Array to store the input line of text
    int count = 0; // Variable to store the count of occurrences of two vowels in succession
    int i; // Loop counter

    // Prompt the user to enter a line of text
    printf("Enter a line of text: ");
    fgets (line, sizeof(line), stdin); // Read the input line of text and store it in 'line'

    // Iterate through each character of the line
    for (i = 0; line[i] != '\0'; i++) {
        // Convert the current character to lowercase
        char current = tolower(line [i]);

        // Check if the current character and the next character are both vowels
        if ((current == 'a' || current == 'e' || current == 'i' || current == 'o' || current == 'u') &&
            (tolower(line [i + 1]) == 'a' || tolower (line [i + 1]) == 'e' || tolower (line [i + 1]) == 'i' ||
             tolower(line [i + 1]) == 'o' || tolower (line [i + 1]) == 'u')) {
            count++; // Increment count if two vowels are in succession
        }
    }

    // Print the number of occurrences of any two vowels in succession
    printf("Number of occurrences of any two vowels in succession: %d\n", count);

    return 0;
}

Algorithm for Q10code: 

1 Start
2 Include the necessary header file stdio.h for standard input and output functions.
3 Define a recursive function running Sum(int n) to calculate the running sum of the first n natural numbers.
•	If n is 0, return 0 (base case).
•	Otherwise, return the sum of n and the result of recursively calling running Sum() with n-1 (recursive case).
4 Define the main () function.
•	Calculate the running sum of the first 25 natural numbers by calling running Sum(25).
•	Print the calculated running sum.
5 End
This algorithm outlines the steps taken by the program to recursively calculate and print the running sum of the first 25 natural numbers.


**Q11**.
Code.
#include <stdio.h>

int stringToInteger(const char *str) {
    int result = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        result = result * 10 + (str[i] - '0');
    }
    return result;
}

int main() {
    const char *str = "1234";
    int num = stringToInteger(str);
    printf("Converted integer: %d\n", num);
    return 0;
}

Algorithm for Q11 code: 

  1.  Define a function stringToInteger that takes a string as an argument.
   2. Initialize a variable result to 0.
   3. Iterate through each character of the string, starting from index 0.
        Multiply result by 10 to shift it to the left.
        Convert the current character to an integer by subtracting the ASCII code of '0' from it.
        Add the converted integer to result.
   4. Return the result after the iteration.
 5.   In the main function, call the stringToInteger function with the string "1234" as an argument.
   6. Print the returned integer value.

**Q12**
Code.
#include <stdio.h>
#include <stdlib.h> // for qsort()
#include <string.h> // for strcmp()

// function to compare two strings (names)
int compare(const void *a, const void *b) {
    return strcmp(*(const char **)a, *(const char **)b);
}

int main() {
    // array of names
    char *names[] = {"John", "Alice", "Bob", "Charlie", "David"};

    // size of the array
    int n = sizeof(names) / sizeof(names[0]);

    // sort the array using qsort()
    qsort(names, n, sizeof(char *), compare);

    // print the sorted array
    for (int i = 0; i < n; i++) {
        printf("%s\n", names[i]);
    }

    return 0;
}

Algorithm for code 12;

1.    Define an array of strings to store the names.
2.Prompt the user to enter the names, storing each name in the array.
3.  Use the qsort() function from the C standard library to sort the array of names.
        Define a comparison function that takes two strings as arguments and returns an integer indicating whether the first string should be sorted before or after the second string.
        Pass a pointer to the comparison function as an argument to qsort().
4.    Print the sorted array of names.

**Q13**
Code.
#include <stdio.h>
#include <string.h>

void PrintArray(char* arr[], int n) {
    for (int i = 0; i < n; i++) {
        printf("%s ", arr[i]);
    }
}

void ReverseString(char* str) {
    int len = strlen(str);
    for (int i = 0; i < len / 2; i++) {
        char temp = str[i];
        str[i] = str[len - 1 - i];
        str[len - 1 - i] = temp;
    }
}

void ReverseArray(char* arr[], int n) {
    for (int i = 0; i < n; i++) {
        ReverseString(arr[i]);
    }
}

int main() {
    char* s[] = {
        "To err is human...",
        "But to really mess things up...",
        "One needs to know C!"
    };
    int n = sizeof(s) / sizeof(s[0]);

    printf("Original strings:\n");
    PrintArray(s, n);
    printf("\n");

    ReverseArray(s, n);

    printf("Reversed strings:\n");
    PrintArray(s, n);

    return 0;
}

Algorithm. Q13

1. Initialize an array of pointers to strings (char* s[]) with the given strings.
2. Calculate the number of strings in the array (n) using sizeof(s) / sizeof(s[0]).
3. Define a function called PrintArray that prints the strings in the array.
4. Define a function called ReverseString that reverses a single string:
    Get the length of the string using strlen.
    Swap characters from the beginning and end of the string until the middle is reached.
5. Define a function called ReverseArray that reverses all strings in the array:
   Iterate through each string in the array.
   Call the ReverseString function to reverse the current string.
6. In the main function:
    Print the original strings using PrintArray.
    Call ReverseArray to reverse all strings.
    Print the resulting reversed strings.

**Q14**
Code.
#include <stdio.h>

int main() {
    char input[80], output[80];
    int i, j = 0;

    printf("Enter the sentence (up to 80 characters): ");
    gets(input);

    for (i = 0; input[i] != '\0'; i++) {
        if (input[i] == 'a' || input[i] == 'e' || input[i] == 'i' || input[i] == 'o' || input[i] == 'u') {
            // Skip vowels
            continue;
        }
        output[j++] = input[i];
    }

    output[j] = '\0'; // Null-terminate the output string

    printf("Sentence after removing vowels: %s\n", output);
    return 0;
}

Algorithm 14:


1.Initialize two character arrays: input[80] to store the input sentence and output[80] to store the modified sentence without vowels.
2.Read the input sentence from the user using gets(input).
3.Iterate through each character in the input array:
If the character is a vowel (‘a’, ‘e’, ‘i’, ‘o’, or ‘u’), skip it.
Otherwise, add the character to the output array.
4.Null-terminate the output array by setting output[j] = '\0'.
5.Print the resulting sentence without vowels using printf("Sentence after removing vowels: %s\n", output).

**Q15**
Code.

#include <stdio.h>
#include <string.h>
#include <ctype.h>

int count_two_vowels(const char *text) {
    int count = 0;
    int i = 0;
    while (text[i] != '\0') {
        if (isalpha(text[i]) && isalpha(text[i+1])) {
            if ((text[i] == 'a' || text[i] == 'e' || text[i] == 'i' || text[i] == 'o' || text[i] == 'u') &&
                (text[i+1] == 'a' || text[i+1] == 'e' || text[i+1] == 'i' || text[i+1] == 'o' || text[i+1] == 'u')) {
                count++;
            }
        }
        i++;
    }
    return count;
}

int main() {
    char text[100];
    printf("Enter a line of text: ");
    fgets(text, sizeof(text), stdin);
    int count = count_two_vowels(text);
    printf("The number of occurrences of two vowels in succession is: %d\n", count);
    return 0;
}

Algorithm 15

1.    Declare a variable to store the count of occurrences, and initialize it to 0.
2.    Iterate through each character in the line of text.
3.    For the current character, check if it is a vowel (using an if statement).
4.    If it is a vowel, check if the next character is also a vowel.
5.    If the next character is also a vowel, increment the count variable.
6.    Repeat steps 2-5 for all characters in the line of text.
7.    Print the value of the count variable as the number of occurrences of two vowels in succession.

