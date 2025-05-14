# Experiment No: 7c – Tower of Hanoi using Recursion

## AIM:
To write a Python program to solve the Tower of Hanoi problem and display all moves using recursive function.

---

## ALGORITHM:
1. Define a recursive function `TowerOfHanoi(n, source, destination, auxiliary)`.
2. If `n > 0`, perform the following steps:
   - Move `n-1` disks from `source` to `auxiliary` using `destination` as auxiliary.
   - Print move from `source` to `destination` for the nth disk.
   - Move `n-1` disks from `auxiliary` to `destination` using `source` as auxiliary.

---

## PROGRAM:
```python
def TowerOfHanoi(n, source, destination, auxiliary):
    if n > 0:
        TowerOfHanoi(n-1, source, auxiliary, destination)
        print(f"Move disk from {source} to {destination}")
        TowerOfHanoi(n-1, auxiliary, destination, source)

n = int(input())
print("No. of disks =", n)
TowerOfHanoi(n, 'A', 'C', 'B')
```

### OUTPUT
![image](https://github.com/user-attachments/assets/6fa28395-3ee8-4808-9eae-b035a787176d)


### RESULT
Thus, the Python program to solve the Tower of Hanoi problem using recursion was successfully executed and displayed the correct disk moves.
