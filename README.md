# Binary Search Algorithm
This repository contains a Python implementation of the binary search algorithm, which is a highly efficient method for finding a specific value in a sorted list or array. Binary search is significantly faster than naive search for large datasets.

## Overview
Naive Search: The naive_search function scans the entire list and checks if each element is equal to the target. If a match is found, it returns the index; otherwise, it returns -1.

Binary Search: The binary_search function uses a divide and conquer approach. It leverages the fact that the list is sorted to efficiently locate the target value.

## Usage
To use the binary search algorithm, simply call the binary_search function with a sorted list and the target value you want to find. It will return the index of the target element in the list if found, or -1 if not found.

```
sorted_list = [1, 3, 5, 10, 12]
target = 10

result = binary_search(sorted_list, target)
if result != -1:
    print(f"Target {target} found at index {result}")
else:
    print(f"Target {target} not found in the list")
```

## Performance Comparison
In this repository, we also compare the performance of naive search and binary search for a sorted list of 10,000 elements. The results demonstrate the significant speed advantage of binary search.

```
# Performance comparison for a sorted list of 10,000 elements
length = 10000

# Build a sorted list
sorted_list = set()
while len(sorted_list) < length:
    sorted_list.add(random.randint(-3 * length, 3 * length))
sorted_list = sorted(list(sorted_list))

# Measure time for naive search
start = time.time()
for target in sorted_list:
    naive_search(sorted_list, target)
end = time.time()
print("Naive search time: ", (end - start) / length, "seconds")

# Measure time for binary search
start = time.time()
for target in sorted_list:
    binary_search(sorted_list, target)
end = time.time()
print("Binary search time: ", (end - start) / length, "seconds")
```

The binary search algorithm consistently outperforms the naive search algorithm for large datasets, making it an essential tool for efficiently finding values in sorted lists or arrays.
Feel free to explore the code and experiment with different datasets to see the advantages of binary search firsthand.
