# Complexity Analyser
I've created a comprehensive Time Complexity Analyzer web tool with the following features:
## Key Features
🔍 Multi-language Support: JavaScript, Python, Java, C++, C, C#, Go, and Rust
⚡ Real-time Analysis:

Detects nested loops and calculates complexity accordingly
Identifies recursive patterns (linear, exponential, divide-and-conquer)
Recognizes built-in method complexities
Analyzes code structure and nesting levels

📊 Detailed Results:

Complexity Badge: Shows the final time complexity (O(1), O(n), O(n²), etc.)
Detailed Explanation: Explains WHY the code has that complexity
Performance Impact: Shows how the algorithm scales with different input sizes
Optimization Tips: Provides specific suggestions for improvement

🎨 Modern UI:

Beautiful gradient design with glassmorphism effects
Responsive layout that works on all devices
Interactive complexity chart showing common time complexities
Code syntax highlighting and clean formatting

How it Works:

Pattern Recognition: Uses regex patterns to identify loops, recursion, and built-in methods specific to each programming language.

Nesting Analysis: Tracks loop nesting levels by counting braces and control structures to determine if it's O(n), O(n²), O(n³), etc.
Recursion Detection: Identifies recursive function calls and determines if they're:

Linear recursion (single recursive call) → O(n)
Exponential recursion (multiple recursive calls like Fibonacci) → O(2ⁿ)
Divide-and-conquer (splitting input in half) → O(log n)


Built-in Method Analysis: Recognizes language-specific methods and their complexities:

Array.sort() → O(n log n)
Array.indexOf() → O(n)
dict.get() → O(1)


Complexity Combination: Takes the highest complexity found among all patterns

Example Usage:
Input: Bubble sort algorithm

```javascript
function bubbleSort(arr) {
    for (let i = 0; i < arr.length; i++) {
        for (let j = 0; j < arr.length - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
            }
        }
    }
    return arr;
}
```

Output:

Complexity: O(n²)
Explanation: "Nested loops detected - outer loop runs n times, inner loop runs n-1 times for each iteration"
Performance: "n=1000 → 1M operations"
Optimization: "Consider more efficient sorting algorithms like quicksort or mergesort"

The tool also includes:

Visual complexity chart showing the relationship between different time complexities
Quick reference examples for common complexity patterns
Performance scaling examples with actual numbers
Mobile-responsive design that works on any device

Just paste your code, select the programming language, click "Analyze Complexity," and get instant detailed analysis with actionable optimization suggestions!