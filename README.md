# C++ Pattern Programs

This repository contains five beginner-friendly C++ snippets for printing square, triangle, and number patterns. Each snippet uses nested loops: the outer loop controls the rows, and the inner loop prints the symbols or numbers in each row.

## Pattern collection

### 1. Square of asterisks

**File:** `square_star_pattern.cpp`  
**Method:** `printSquarePattern(n)`

Prints `n` rows, each containing `n` asterisks.

```text
* * *
* * *
* * *
```

### 2. Right-angled triangle of asterisks

**File:** `right_angle_triangle_asterisk_pattern.cpp`  
**Method:** `printRightAngledTrianglePattern(n)`

Each row adds one asterisk, starting with one.

```text
*
* *
* * *
```

### 3. Inverted right-angled triangle of asterisks

**File:** `Inverted_Right-angel_triangle_Asterisk_Pattern.cpp`  
**Method:** `printInvertedRightAngledTrianglePattern(n)`

Each row has one fewer asterisk than the previous row.

```text
* * *
* *
*
```

### 4. Right-angled triangle repeating the row number

**File:** `right_angled_number_triangle.cpp`  
**Method:** `printRightAngledNumberTriangle(n)`

Each row repeats its row number.

```text
1
2 2
3 3 3
```

### 5. Right-angled triangle of column numbers

**File:** `right_angle_triangle_with_column_numbers.cpp`  
**Method:** `printTriangle(n)`

Each row prints numbers from `1` up to that row number.

```text
1
1 2
1 2 3
```

## How to use

These files define pattern-printing methods but do not include a `main()` function. To run one, include its source file in a small driver program and call the method:

```cpp
#include "right_angle_triangle_asterisk_pattern.cpp"

int main() {
    solution pattern;
    pattern.printRightAngledTrianglePattern(3);
}
```

Compile the driver program with a C++ compiler, such as:

```sh
g++ -std=c++17 main.cpp -o pattern
```

Then run the resulting executable. The examples use `n = 3`; change the argument to print a different number of rows.

## Input and complexity

The methods accept an integer `n`. For positive `n`, they print the requested pattern to standard output. For `n <= 0`, the loops do not run, so nothing is printed.

All patterns take **O(n²)** time in the general case. They use **O(1)** additional space, not including the output sent to the console.

## Notes

- Each source file declares a class named `solution`. Include one pattern file per program to avoid duplicate class definitions.
- The snippets use `<bits/stdc++.h>`, a convenience header supported by GCC and some other compilers. It is not part of the C++ standard; on other compilers, replace it with the specific headers you need, such as `<iostream>`.
- The inverted pattern filename uses `angel`; the method name uses the correctly spelled `Angled`.
