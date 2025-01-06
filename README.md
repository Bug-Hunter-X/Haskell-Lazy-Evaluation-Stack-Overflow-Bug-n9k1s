# Haskell Lazy Evaluation Stack Overflow

This repository demonstrates a common error in Haskell programming involving lazy evaluation and infinite lists.  The `bug.hs` file contains code that attempts to process an infinite list of ones using the `take` function. This results in a stack overflow because Haskell attempts to evaluate the entire infinite list before summing its elements.  The `bugSolution.hs` file provides a corrected version that uses a more appropriate method to handle the infinite list.

## Bug Description
The bug stems from an incorrect use of `take` with an infinite list.   Lazy evaluation does not prevent a stack overflow when attempting to force evaluation of an infinitely large data structure directly.

## Solution
The solution avoids creating a large intermediate list in memory. The correct approach processes the list element-by-element to prevent a stack overflow.