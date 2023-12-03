
# Time Complexity and Space Complexity Overview

## Time Complexity:

### Definition:
Time complexity measures the rate at which the time taken by an algorithm increases concerning the input size.

### Importance:
- **Interviews:** Algorithms are often evaluated based on time complexity during coding interviews.
- **Performance:** Understanding time complexity helps in writing efficient and scalable code.

### Factors:
- **Not Time Taken:** Time complexity is not equivalent to the actual time taken, as it depends on the machine and configuration.
- **Rate of Increase:** It represents the rate at which the time taken increases concerning the input size.

### Big O Notation:
- Expresses time complexity as `O(f(n))`, where `f(n)` is the rate of increase.
- Avoids constants and lower values for simplicity.

| Big-Oh (O)  | Theta(Θ)       | Omega(Ω)       |
|-------------|----------------|----------------|
| Upper Bound | Average Case   | Lower Bound    |


### Three Rules:
1. **Worst Case Scenario:** Always compute time complexity in terms of the worst case.
2. **Avoid Constants:** Disregard constant factors during analysis.
3. **Avoid Lower Values:** Do not consider lower values that don't significantly affect complexity.

### Example:
```cpp
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        // Code block
    }
}
// Time Complexity: O(n^2)
```

```cpp
for (int i = 0; i < n; i++) {
    for (int j = 0; j <= i; j++) {
        // Code block
    }
}

// i=0 [j=0]
// i=1 [j=0,1]
// i=2 [j=0,1,2]
// i=n-1 [j=0,1,2,...n-1] 

// N x (N+1) /2

// Time Complexity: O((n^2)/2) = O(n^2)
```

## Space Complexity:
### Definition:
Space complexity measures the memory space an algorithm uses concerning the input size.

### Components:
1. **Auxiliary Space:** Extra space used to solve the problem.
2. **Input Space:** Space required to store the input.

### Big O Notation:
- Expressed as `O(f(n))`, where `f(n)` is the total space complexity.
- Similar rules as time complexity (avoid constants, lower values).

### Best Practice:
- Avoid manipulating input data to ensure code reliability in software engineering.

## Example:

```cpp
void exampleFunction(int n) {
    int* arr = new int[n]; // Auxiliary space
    // Code block using the array
    delete[] arr; // Deallocate memory
}
// Space Complexity: O(n)
```



### Important Note:

In competitive programming, note that servers generally take around one second for roughly 10^8 operations. Keep this in mind when analyzing the time complexity of your code.
