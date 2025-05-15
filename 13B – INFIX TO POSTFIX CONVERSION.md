# Experiment No: 13b – Infix to Postfix Conversion

## AIM:
To write a Python program to convert a given infix expression to postfix expression using dictionary for precedence and set for operators.

---

## ALGORITHM:
1. Define a set `op` to include valid operators: `|`, `%`, `*`, `(`, `)`.
2. Define a dictionary `pri` to set the precedence for operators.
3. Create a function `in_to_post(exp)` to convert infix to postfix.
4. Traverse each character in the input expression:
   - If the character is an operand, append to output.
   - If it is `'('`, push to stack.
   - If it is `')'`, pop from stack to output until `'('` is encountered.
   - If it is an operator, pop from stack to output based on precedence, then push the current operator.
5. After traversal, pop any remaining operators in the stack to the output.

---

## PROGRAM:
```python
op = set(['|', '%', '*', '(', ')'])
pri = {'|': 1, '%': 2, '*': 2}

def in_to_post(exp):
    stack = []
    out = ''
    for char in exp:
        if char not in op:
            out += char
        elif char == '(':
            stack.append('(')
        elif char == ')':
            while stack and stack[-1] != '(':
                out += stack.pop()
            stack.pop()
        else:
            while stack and stack[-1] != '(' and pri[char] <= pri[stack[-1]]:
                out += stack.pop()
            stack.append(char)
    while stack:
        out += stack.pop()
    return out

exp = input()
print(f"infix notation:  {exp}")
print(f"postfix notation:  {in_to_post(exp)}")
```

### OUTPUT
![image](https://github.com/user-attachments/assets/989ee50f-4280-41d6-a624-a1300353bac2)


### RESULT
Thus, the Python program to convert infix expression to postfix expression was successfully executed following precedence and associativity rules.
