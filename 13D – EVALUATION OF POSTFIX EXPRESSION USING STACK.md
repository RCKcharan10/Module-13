# Experiment No: 13d – Evaluation of Postfix Expression using Stack

## AIM:
To write a Python program to evaluate a given postfix expression that contains Multiplication and Addition operators using stack.

---

## ALGORITHM:
1. Define a set of operators.
2. Traverse the postfix expression.
3. If the character is an operand, push it to the stack.
4. If it is an operator, pop two operands from the stack, evaluate the result, and push it back.
5. Return the final value from the stack.

---

## PROGRAM:
```python
OPERATORS = set(['*', '-', '+', '%', '/', '**'])

def evaluate_postfix(expression):
    stack = []
    for i in expression:
        if i not in OPERATORS:
            stack.append(i)
        else:
            a = stack.pop()
            b = stack.pop()
            if i == '+':
                res = int(b) + int(a)
            elif i == '-':
                res = int(b) - int(a)
            elif i == '*':
                res = int(b) * int(a)
            elif i == '%':
                res = int(b) % int(a)
            elif i == '/':
                res = int(b) / int(a)
            elif i == '**':
                res = int(b) ** int(a)
            stack.append(res)
    return stack[0]

expression = input()
print('postfix expression: ', expression)
print('Evaluation result: ', evaluate_postfix(expression))

```


### OUTPUT
![image](https://github.com/user-attachments/assets/94f6a562-e75b-4768-b886-42f0982f44f9)

### RESULT
Thus, the Python program for evaluating a postfix expression using stack was successfully executed and the output was verified.
