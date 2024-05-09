Solution
Part 1
In the first stage of development, I created a basic function called ‘hypotenuse’ that takes two arguments representing the lengths of the two legs of a right triangle.
I implemented the calculation of the hypotenuse using the Pythagorean theorem:
C = a**2 + b**2.
And then I tested ‘hypotenuse’ function with some inputs.
Learning Journal:
-	Test 1 : ‘hypotenuse(3, 4)’ returned ‘5.0’
-	Test 2 : ‘hypotenuse(5, 12)’ returned ‘13.0’
-	Test 3 : ‘hypotenuse(8, 15)’ returned ‘17.0’
Input
def hypotenuse(a, b):
    pass
import math
def hypotenuse(a, b):
    return math.sqrt(a**2 + b**2)
print(hypotenuse(3, 4))
# Output should be 5.0
print(hypotenuse(5, 12))
# Output should be 13.0
print(hypotenuse(8, 15))
Output 
5.0
13.0
17.0
PS C:\Users\rachi\OneDrive\Documents\main.py>
Part 2.
Let’s create a function that calculates the factorial of a given nonnegative integer.
I start by implementing a basic version of the factorial function and then use a simple recursive approach to calculate the factorial.
Input
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)
# Test the function
print(factorial(5))
Output
120
PS C:\Users\rachi\OneDrive\Documents\main.py>
•	I define a function called ‘factorial’ that takes an integer ‘n’ as input. If ‘n’ is 0, the function returns 1. Otherwise, it returns ‘n’ multiplied by the factorial of ‘n-1’.
•	I added an error handling to ensure that the input is nonnegative integer.
Input
def factorial(n):
    if not isinstance(n, int) or n < 0:
        return "Input must be a non-negative integer"
    elif n == 0:
        return 1
    else:
        return n * factorial(n-1)
# Test the function
print(factorial(5)) # 
print(factorial(-1))
Output
120
Input must be a non-negative integer
PS C:\Users\rachi\OneDrive\Documents\main.py>
•	I use ‘isinstance’ to check if the input is an integer.
•	Added a condition to check if n is less than 0, returning an error message if it is.
To improve efficiency and reduce the risk of the stack overflow for large inputs, I switched to an iterative approach.
Input
def factorial(n):
    if not isinstance(n, int) or n < 0:
        return "Input must be a non-negative integer"
    else:
        result = 1
        for i in range(1, n+1):
            result *= i
        return result
# Test the function
print(factorial(5))
print(factorial(0))   
print(factorial(10))
Output
120
1
3628800
PS C:\Users\rachi\OneDrive\Documents\main.py>
I used ‘for’ loop to iterate from 1 to ‘n’ and then multiply ‘result’ by ‘i’ in each iteration to calculate the factorial.
By incrementally developing our factorial function, we've created a versatile and efficient solution for calculating factorials.
