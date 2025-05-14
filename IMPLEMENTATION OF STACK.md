# Experiment No: 31 – Stack Implementation using List

## AIM:
To write a Python program to implement a stack using list and its built-in methods `append()` and `pop()`.

---

## ALGORITHM:
1. Define a class named `st` to represent the stack.
2. Inside the class:
   - Define the method `push(L)` to append even numbers from 1 to L into the stack.
   - Define the method `pop()` to remove the top element from the stack and display it.
   - Define the method `peek()` to display current elements of the stack.
3. Create an instance of the class.
4. Get input value `L` from the user.
5. Call `push(L)` to populate the stack with even numbers up to `L`.
6. Call `peek()` to show the stack elements.
7. Call `pop()` to remove the top element.
8. Call `peek()` again to display updated stack.

---

## PROGRAM:
```python
stack = []
class st:
    def push(self, L):
        for i in range(1, L):
            if i % 2 == 0:
                stack.append(i)
    def pop(self):
        print(f"Element popped :  {stack.pop()}")
    def peek(self):
        print(f"Elements in the stack \n {stack}")

L = int(input())
no = st()
no.push(L)
no.peek()
no.pop()
no.peek()
```

## OUTPUT
![image](https://github.com/user-attachments/assets/058cc6dd-919e-4964-ba40-185dc8c9aa61)

RESULT:
Thus, the Python program to implement a stack using a list and built-in methods was successfully executed.
