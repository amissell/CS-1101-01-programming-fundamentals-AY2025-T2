Hello everyone,

For this assignment, I will be using Python 3.13.0 and writing my code in Visual Studio Code (VS Code). In this post, I will explore and explain the behavior of various Python statements and compare the differences between Python 2 and Python 3.

Explanation of Statements and Outputs
Input 1:

print 'Hello, World1'
Output:


File "<python-input-4>", line 1
    print 'hello world'
    ^^^^^^^^^^^^^^^^^^^
SyntaxError: Missing parentheses in call to 'print'. Did you mean print(...)?
Explanation:

In Python 2, the print statement didn't require parentheses. For example, print 'Hello, World!' would work fine.
In Python 3, the print statement was changed to a function, so it requires parentheses around the argument.
The correct syntax in Python 3 is:

print('Hello, World!')

Input 2:
1 / 2

Output:
0.5

Explanation:

In Python 2, to get a float result from division, you needed to explicitly use a floating-point number, such as 1.0 / 2.
In Python 3, division between two integers always results in a float. Therefore, 1 / 2 gives 0.5 instead of 0 as it would in Python 2.

Input 3:
type(1 / 2)

Output:
<class 'float'>

Explanation:

In Python 2, division between two integers returns an integer. So, 1 / 2 would return an integer type (<class 'int'>).
In Python 3, the type() function shows that 1 / 2 results in a float, as Python 3 performs floating-point division by default.

Input 4:
print(01)

Output:
File "<python-input-7>", line 1
    print(01)
           ^
SyntaxError: leading zeros in decimal integer literals are not permitted; use an 0o prefix for octal integers

Explanation:

In Python 2, leading zeros were allowed and treated as octal numbers (base 8). So, 01 would work.
In Python 3, leading zeros in decimal integer literals are not allowed. This results in a syntax error. To represent octal numbers.
To avoid the error, simply write 1 instead of 01.

Input 5:
1 / (2 / 3)

Output:
1.5

Explanation:

Both in Python 2 and Python 3, division between floating-point numbers produces a float result. In this case, 2 / 3 results in approximately 0.6666, and then 1 / 0.6666 results in 1.5.
The behavior is the same in both Python 2 and Python 3.

Question:
Do you think it's beneficial to adapt to Python 3's behavior, or should there still be use cases for Python 2?


Reference:
Downey, A. (2015). Think Python: How to think like a computer scientist (2nd ed.). Green Tea Press. https://greenteapress.com/thinkpython2/thinkpython2.pdf