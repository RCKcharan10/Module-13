# Experiment No: 13e – Evaluation of Prefix Expression using Stack

## AIM:
To write a Python program to evaluate a user-given prefix expression using stack.

---

## ALGORITHM:
1. Define a set of valid operators.
2. Traverse the prefix expression in reverse.
3. If a character is an operand, push it to the stack.
4. If it's an operator, pop two operands, evaluate, and push the result.
5. Return the final result from the stack.

---

## PROGRAM:
```python
op = set(['*', '-', '+', '%', '/', '**'])

def evaluate(exp):
    stack = []
    for c in exp[::-1]:
        if c not in op:
            stack.append(int(c))
        else:
            o1 = stack.pop()
            o2 = stack.pop()
            if c == '+':
                stack.append(o1 + o2)
            if c == '-':
                stack.append(o1 - o2)
            if c == '%':
                stack.append(o1 % o2)
            if c == '/':
                stack.append(o1 / o2)
            if c == '*':
                stack.append(o1 * o2)
            if c == '**':
                stack.append(o1 ** o2)
    return stack.pop()

test = input()
print("Prefix Expression :", test)
print("Evaluation result :", evaluate(test))

```

### OUTPUT
![image](https://github.com/user-attachments/assets/268978cf-e188-41c0-92cc-1e7d09e7aef3)

### RESULT
Thus, the Python program to evaluate a prefix expression using stack was executed successfully and verified.
