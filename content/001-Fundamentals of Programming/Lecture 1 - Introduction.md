# Exercise 1
- Read a string from the keyboard
- Separate by spaces
- Output negative numbers, name, prime numbers in order with no duplicates
```python
import math

def is_prime(number: int) -> bool:
    if number < 2:
        return False
    if number == 2:
        return True
    if number % 2 == 0:
        return False
    for i in range(3, int(math.sqrt(number)) + 1, 2):
        if number % i == 0:
            return False
    return True


def is_capitalized(word: str) -> bool:
    return 'A' <= word[0] <= 'Z'

# 45 Anna has apples -13 17 23 23 Mary
line = input("Enter a string: ")
tokens = line.split(" ")
negative_numbers = []
prime_numbers = []
names = []
for token in tokens:
    try:
        int_token = int(token)
        if int_token < 0:
            negative_numbers.append(int_token)
        elif is_prime(int_token):
            prime_numbers.append(int_token)
    except ValueError:
        if is_capitalized(token):
            names.append(token)
print("Negative numbers:", negative_numbers)
prime_numbers = set(prime_numbers)
prime_numbers = list(prime_numbers)
prime_numbers.sort()
print("Prime numbers:", set(prime_numbers))
print("Names:", names)

```