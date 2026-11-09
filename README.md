
C++ Pattern Programs

A small collection of C++ classes that print common star and number patterns. Each source file defines a  solution  class with a public method that accepts  n  and writes the pattern to standard output.

Patterns

┌────────────────────────────────────────────────────┬────────────────────────────────────────────┬──────────────────────────────────────────────────┐
│ Source file                                        │ Method                                     │ Output                                           │
├────────────────────────────────────────────────────┼────────────────────────────────────────────┼──────────────────────────────────────────────────┤
│ square_star_pattern.cpp                            │ printSquarePattern(n)                      │ An n by n square of * symbols                    │
├────────────────────────────────────────────────────┼────────────────────────────────────────────┼──────────────────────────────────────────────────┤
│ right_angle_triangle_asterisk_pattern.cpp          │ printRightAngledTrianglePattern(n)         │ A left-aligned triangle of * symbols, growing    │
│                                                    │                                            │ from 1 to n per row                              │
├────────────────────────────────────────────────────┼────────────────────────────────────────────┼──────────────────────────────────────────────────┤
│ Inverted_Right-angel_triangle_Asterisk_Pattern.cpp │ printInvertedRightAngledTrianglePattern(n) │ An inverted left-aligned triangle of * symbols,  │
│                                                    │                                            │ shrinking from n to 1 per row                    │
├────────────────────────────────────────────────────┼────────────────────────────────────────────┼──────────────────────────────────────────────────┤
│ right_angled_number_triangle.cpp                   │ printRightAngledNumberTriangle(n)          │ A triangle where row i repeats the number i, i   │
│                                                    │                                            │ times                                            │
├────────────────────────────────────────────────────┼────────────────────────────────────────────┼──────────────────────────────────────────────────┤
│ right_angle_triangle_with_column_numbers.cpp       │ printTriangle(n)                           │ A triangle where row i contains the numbers from │
│                                                    │                                            │ 1 through i                                      │
└────────────────────────────────────────────────────┴────────────────────────────────────────────┴──────────────────────────────────────────────────┘

For example, the growing asterisk triangle with  n = 4  prints:

*
* *
* * *
* * * *

Each symbol in the source output is followed by a space.

Using a pattern

These files are snippets, not standalone programs: they do not define  main() . Each file also declares a class named  solution , so include only the pattern you want to use in a given program.

#include "right_angle_triangle_asterisk_pattern.cpp"

int main() {
    solution pattern;
    pattern.printRightAngledTrianglePattern(4);
}

Compile with a C++ compiler, for example:

g++ -std=c++17 main.cpp -o pattern


All patterns take O(n²) time in the general case. They use O(1) additional space, not including the output sent to the console.

Notes

• Each source file declares a class named  solution . Include one pattern file per program to avoid duplicate class definitions.
• The snippets use  <bits/stdc++.h> , a convenience header supported by GCC and some other compilers. It is not part of the C++ standard; on other compilers, replace it with the specific headers you need, such as  <iostream> .
• The inverted pattern filename uses  angel ; the method name uses the correctly spelled  Angled .
