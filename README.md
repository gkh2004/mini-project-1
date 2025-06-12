# mini-project-1
python assignment
# Initial list
L = [11, 12, 13, 14]

# (i) Add 50 and 60 to L
L.append(50)
L.append(60)
# Alternatively: L.extend([50, 60])

# (ii) Remove 11 and 13 from L
L.remove(11)
L.remove(13)

# (iii) Sort L in ascending order
L.sort()
print("Ascending:", L)

# (iv) Sort L in descending order
L.sort(reverse=True)
print("Descending:", L)

# (v) Search for 13 in L
if 13 in L:
    print("13 is in the list")
else:
    print("13 is not in the list")

# (vi) Count the number of elements present in L
print("Count of elements:", len(L))

# (vii) Sum all the elements in L
print("Sum of all elements:", sum(L))

# (viii) Sum all ODD numbers in L
odd_sum = sum(x for x in L if x % 2 != 0)
print("Sum of odd numbers:", odd_sum)

# (ix) Sum all EVEN numbers in L
even_sum = sum(x for x in L if x % 2 == 0)
print("Sum of even numbers:", even_sum)

# (x) Sum all PRIME numbers in L
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

prime_sum = sum(x for x in L if is_prime(x))
print("Sum of prime numbers:", prime_sum)

# (xi) Clear all the elements in L
L.clear()
print("List after clearing:", L)

# (xii) Delete L
del L
# print(L)  # This would raise an error since L is deleted
# Initial dictionary
D = {1: 5.6, 2: 7.8, 3: 6.6, 4: 8.7, 5: 7.7}

# (i) Add new entry: key = 8, value = 8.8
D[8] = 8.8
print("After adding key=8:", D)

# (ii) Remove key = 2
D.pop(2, None)  # Using pop with default to avoid KeyError if key is missing
print("After removing key=2:", D)

# (iii) Check whether key = 6 is present
if 6 in D:
    print("Key 6 is present in D.")
else:
    print("Key 6 is not present in D.")

# (iv) Count the number of elements in D
print("Number of elements in D:", len(D))

# (v) Add all the values present in D
print("Sum of all values in D:", sum(D.values()))

# (vi) Update value of key 3 to 7.1
D[3] = 7.1
print("After updating key=3:", D)

# (vii) Clear the dictionary
D.clear()
print("After clearing D:", D)
# Convert lists to sets
S1 = set([10, 20, 30, 40, 50, 60])
S2 = set([40, 50, 60, 70, 80, 90])

# (i) Add 55 and 66 in Set S1
S1.add(55)
S1.add(66)
print("After adding 55 and 66 to S1:", S1)

# (ii) Remove 10 and 30 from Set S1
S1.discard(10)  # discard doesn't raise an error if element is not found
S1.discard(30)
print("After removing 10 and 30 from S1:", S1)

# (iii) Check whether 40 is present in S1
if 40 in S1:
    print("40 is present in S1.")
else:
    print("40 is not present in S1.")

# (iv) Find the union between S1 and S2
union_set = S1.union(S2)
print("Union of S1 and S2:", union_set)

# (v) Find the intersection between S1 and S2
intersection_set = S1.intersection(S2)
print("Intersection of S1 and S2:", intersection_set)

# (vi) Find the difference S1 - S2
difference_set = S1.difference(S2)
print("S1 - S2:", difference_set)
import random
import string

for _ in range(100):
    length = random.randint(6, 8)
    rand_str = ''.join(random.choices(string.ascii_letters + string.digits, k=length))
    print(rand_str)
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

for num in range(600, 801):
    if is_prime(num):
        print(num)
for num in range(100, 1001):
    if num % 7 == 0 and num % 9 == 0:
        print(num)
import random

# Generate two lists of 10 random integers between 10 and 30
list1 = [random.randint(10, 30) for _ in range(10)]
list2 = [random.randint(10, 30) for _ in range(10)]

print("List 1:", list1)
print("List 2:", list2)

# (i) Common numbers in the two lists
common = list(set(list1) & set(list2))
print("Common numbers:", common)

# (ii) Unique numbers in both the lists
unique = list(set(list1) ^ set(list2))  # symmetric difference
print("Unique numbers in both lists:", unique)

# (iii) Minimum in both the lists
print("Minimum in List 1:", min(list1))
print("Minimum in List 2:", min(list2))

# (iv) Maximum in both the lists
print("Maximum in List 1:", max(list1))
print("Maximum in List 2:", max(list2))

# (v) Sum of both the lists
print("Sum of List 1:", sum(list1))
print("Sum of List 2:", sum(list2))
print("Total Sum of both lists:", sum(list1) + sum(list2))
import random

# Generate a list of 100 random integers between 100 and 900
numbers = [random.randint(100, 900) for _ in range(100)]
print("Generated Numbers:", numbers)

# Function to check if a number is prime
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

# (i) All odd numbers
odd_numbers = [num for num in numbers if num % 2 != 0]
print("\nOdd Numbers ({}):".format(len(odd_numbers)), odd_numbers)

# (ii) All even numbers
even_numbers = [num for num in numbers if num % 2 == 0]
print("\nEven Numbers ({}):".format(len(even_numbers)), even_numbers)

# (iii) All prime numbers
prime_numbers = [num for num in numbers if is_prime(num)]
print("\nPrime Numbers ({}):".format(len(prime_numbers)), prime_numbers)
# Define the dictionary
D = {1: "One", 2: "Two", 3: "Three", 4: "Four", 5: "Five"}

# Open a file for writing
with open("dictionary_output.txt", "w") as file:
    for key, value in D.items():
        file.write(f"{key}, {value}\n")

print("Dictionary written to 'dictionary_output.txt' in required format.")
# Define the list (using set notation in your example, assuming you meant list or set)
L = {"One", "Two", "Three", "Four", "Five"}  # It's actually a set due to {}

# Open a file for writing
with open("list_lengths.txt", "w") as file:
    for item in L:
        file.write(f"{item}, {len(item)}\n")

print("Element lengths written to 'list_lengths.txt'.")
import random
import string

# Open a file for writing
with open("random_strings.txt", "w") as file:
    for _ in range(100):
        length = random.randint(10, 15)
        rand_str = ''.join(random.choices(string.ascii_letters + string.digits, k=length))
        file.write(rand_str + "\n")

print("100 random strings written to 'random_strings.txt'.")
# Function to check if a number is prime
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

# Open file to write prime numbers
with open("prime_numbers.txt", "w") as file:
    for num in range(600, 801):  # inclusive of 800
        if is_prime(num):
            file.write(str(num) + "\n")

print("Prime numbers between 600 and 800 written to 'prime_numbers.txt'.")
import time

# Record start time
start_time = time.time()

# ---- Program block to be timed ----
# Example: Print squares of numbers from 1 to 100000
for i in range(1, 100001):
    _ = i ** 2
# ------------------------------------

# Record end time
end_time = time.time()

# Calculate elapsed time
elapsed_time = end_time - start_time
print(f"Time taken by the program: {elapsed_time:.4f} seconds")
import random
import time
import matplotlib.pyplot as plt

# List sizes
sizes = [5000, 10000, 15000, 20000, 25000]
times = []

for n in sizes:
    # Generate a random list of n elements
    lst = [random.randint(1, 100000) for _ in range(n)]
    
    start_time = time.time()
    lst.sort()  # Sort the list
    end_time = time.time()
    
    elapsed_time = end_time - start_time
    times.append(elapsed_time)
    print(f"Sorted {n} elements in {elapsed_time:.6f} seconds")

# Plotting the graph
plt.plot(sizes, times, marker='o', linestyle='-', color='b')
plt.title('Time Taken to Sort Lists of Various Sizes')
plt.xlabel('Number of Elements in List')
plt.ylabel('Time Taken (seconds)')
plt.grid(True)
plt.show()
# Dictionary with student names as keys and list of marks in 5 subjects as values
student_marks = {
    "Alice": [85, 90, 78, 92, 88],
    "Bob": [70, 75, 80, 72, 68],
    "Charlie": [95, 100, 98, 97, 96],
    "David": [60, 65, 58, 62, 64],
    "Eva": [88, 84, 90, 86, 85]
}

# Calculate average marks for each student
average_marks = {student: sum(marks)/len(marks) for student, marks in student_marks.items()}

# Find student with maximum average marks
max_student = max(average_marks, key=average_marks.get)
max_average = average_marks[max_student]

# Find student with minimum average marks
min_student = min(average_marks, key=average_marks.get)
min_average = average_marks[min_student]

print(f"Student with maximum average marks: {max_student} ({max_average:.2f})")
print(f"Student with minimum average marks: {min_student} ({min_average:.2f})")


