## MODULE - 7
# EXP 31: Types of Recursion: Head Recursion in Python

##  AIM:
To write a Python program to demonstrate **Head Recursion** by finding and printing the sequence based on the sum of all digits (even or odd adjusted input).

##  ALGORITHM:

1. **Start**
2. Define a recursive function `fun(n)`
3. In the function:
   - Create a recursive call at the **beginning** (Head Recursion)
   - Print the result after the recursive call
4. Take input from the user
5. If input is odd, convert it to the next even number
6. Call the recursive function
7. **Stop**

##  PROGRAM:

```
def fun(n):
    if n == 0:
        return
    fun(n - 2)        
    print(n, end=' ') 

n = int(input())

if n % 2 != 0:
    n += 1

fun(n)
```

## OUTPUT
![image](https://github.com/user-attachments/assets/231d80e5-e0f1-4799-8de5-fceff2d9be43)

## RESULT
Thus, the program is verified successfully.

---

# EXP 32: Recursion:Palindrome Checker Using Recursion in Python

##  AIM:
To write a Python program to check whether a given string is a **palindrome** using **recursion**.



##  ALGORITHM:

1. **Start**
2. Define a recursive function `is_palindrome(word)`
   - **Base Case:** If the string length is less than 1, return `True`
   - **Recursive Case:** If the first and last characters match, call the function recursively on the substring without first and last characters
   - Else, return `False`
3. Get input from the user
4. Call the recursive function
5. Print whether the string is a palindrome
6. **Stop**



##  PROGRAM:
```
def is_palindrome(word):
    if len(word) < 1: 
        return True
    if word[0] == word[-1]: 
        return is_palindrome(word[1:-1])
    else:
        return False

word = input()

if is_palindrome(word):
    print("The string is a palindrome.")
else:
    print("The string is not a palindrome.")
```

## OUTPUT
![image](https://github.com/user-attachments/assets/4d21425a-386e-4a44-8363-d9c710b872a5)

## RESULT
Thus, the program is verified successfully.

---

# EXP 33 : Recursion:Sum of Digits using Recursion in Python

##  AIM:
To write a Python program to calculate the **sum of all digits** in a number using **recursion**.

##  ALGORITHM:

1. **Start**
2. Define a recursive function `sum_digit(n)` that:
   - Returns 0 if `n <= 0` (Base Case)
   - Else, returns `n % 10 + sum_digit(n // 10)` (Recursive Case)
3. Take integer input from the user.
4. Call the recursive function and store the result.
5. Print the result.
6. **Stop**

##  PROGRAM:

```
def sum_digit(n):
    if n <= 0:  
        return 0
    else:  
        return n % 10 + sum_digit(n // 10)

num = int(input())

result = sum_digit(num)
print("Sum of digits:", result)
```
## OUTPUT
![image](https://github.com/user-attachments/assets/448bc511-331b-4cc7-8235-8ed4f035bbf3)

## RESULT
Thus, the program is verified successfully.

---

# EXP 34: Taylor Series Using Recursion in Python

##  AIM:
To write a Python program to evaluate a **Taylor Series** using **recursion**, where values of `x` and `n` are taken from the user.

## ALGORITHM:

1. **Start**
2. Create variables `x` and `n`
3. Get values for `x` and `n` from the user
4. Define a recursive function `series(x, n)`
   - **Base case:** If `n == 0`, return 1
   - **Recursive case:** Return `x**n / n + series(x, n-1)`
5. Print the result
6. **Stop**

## PROGRAM:
```
def series(x, n):
    if n == 0:
        return 1
    else:
        return (x**n) / n + series(x, n-1)

x = int(input())
n = int(input())
print(series(x, n))
```


## OUTPUT
![image](https://github.com/user-attachments/assets/0a0a4288-d4a4-46fe-8045-19ed76038032)

## RESULT
Thus, the program is verified successfully.

---

# EXP 35: Taylor Series:sinh(x) Evaluation using Recursion in Python

##  AIM:
To write a Python program to evaluate the value of **sinh(x)** for **n terms** using recursion.


##  ALGORITHM:

1. **Start**
2. Read input for variable `x` (angle or number)
3. Read input for variable `n` (number of terms)
4. Define a function `fact(n)`:
   - If `n <= 1`, return 1
   - Else, return `n * fact(n - 1)` (recursive factorial)
5. Define a function `sinh(x, n)`:
   - If `n == 0`, return `x`
   - Else, return `(pow(x, 2*n + 1) / fact(2*n + 1)) + sinh(x, n - 1)`
6. Call the `sinh(x, n)` function and print the result
7. **Stop**


##  PROGRAM:

```
def fact(i):
   if i==1 or i==0:
       return 1
   else:
       return i*fact(i-1)
def sinh(x,n):
  if n==0:
    return x
  else:
    return(((pow(x,(2*n+1)))/(fact(2*n+1))) + sinh(x,n-1))
x=int(input())
n=int(input())
print(sinh(x,n))
```

## OUTPUT
![image](https://github.com/user-attachments/assets/ea09add8-56f6-4b0c-b84f-c7fcddece3c2)

## RESULT
Thus, the program is verified successfully.
