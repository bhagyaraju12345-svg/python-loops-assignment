# python-loops-assignment
# Temperature Data Processing & NumPy Tasks

import numpy as np
import time

# -------------------- Task 1 --------------------
print("----- Task 1: Temperature Data Processing -----")

# Create NumPy array
temps_celsius = np.array([22, 25, 28, 24, 26])

# Convert to Fahrenheit
temps_fahrenheit = temps_celsius * 1.8 + 32

# Print arrays
print("Celsius:", temps_celsius)
print("Fahrenheit:", temps_fahrenheit)

# Calculate average in Fahrenheit (rounded to 1 decimal)
avg_fahrenheit = round(np.mean(temps_fahrenheit), 1)
print("Average Fahrenheit:", avg_fahrenheit)


# -------------------- Task 2 --------------------
print("\n----- Task 2: Array Shape and Statistics -----")

scores = np.array([85, 90, 78, 92, 88, 76, 95, 82, 89, 91, 87, 84])

# Shape
print("Shape:", scores.shape)

# Total elements
print("Total elements:", scores.size)

# Highest score
print("Highest score:", np.max(scores))

# Lowest score
print("Lowest score:", np.min(scores))

# Range
range_value = np.max(scores) - np.min(scores)
print("Range:", range_value)


# -------------------- Task 3 --------------------
print("\n----- Task 3: Performance Comparison -----")

# NumPy array
np_array = np.arange(1, 50001)

# Python list
py_list = list(range(1, 50001))

# NumPy sum timing
start_np = time.time()
np_sum = np.sum(np_array)
end_np = time.time()
np_time = round(end_np - start_np, 4)

# Python sum timing
start_py = time.time()
py_sum = sum(py_list)
end_py = time.time()
py_time = round(end_py - start_py, 4)

print("NumPy sum:", np_sum)
print("Python sum:", py_sum)
print("NumPy time:", format(np_time, ".4f"), "seconds")
print("Python time:", format(py_time, ".4f"), "seconds")

# How many times faster
if py_time != 0:
    faster = round(py_time / np_time, 1) if np_time != 0 else "Infinity"
    print("NumPy is", faster, "times faster")
else:
    print("Python time too small to compare")

output of the program
----- Task 1: Temperature Data Processing -----
Celsius: [22 25 28 24 26]
Fahrenheit: [71.6 77.  82.4 75.2 78.8]
Average Fahrenheit: 77.0

----- Task 2: Array Shape and Statistics -----
Shape: (12,)
Total elements: 12
Highest score: 95
Lowest score: 76
Range: 19

----- Task 3: Performance Comparison -----
NumPy sum: 1250025000
Python sum: 1250025000
NumPy time: 0.0002 seconds
Python time: 0.0005 seconds
NumPy is 2.5 times faster
