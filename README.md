# LeetCode 216 - Combination Sum III

## Problem Description

Find all possible combinations of `k` numbers that add up to `n`.

The numbers must be chosen from `1` to `9`.

Each number can be used only once.

The order of the numbers does not matter.

## Example

Input:

k = 3
n = 7

The possible combination is:

[1,2,4]

Because:

1 + 2 + 4 = 7

Output:

[[1,2,4]]

## Approach

We use **Backtracking** to generate possible combinations.

We start with numbers from `1` to `9` and build a combination step by step.

For every number, we add it to the current combination and continue searching with the next number.

After exploring that choice, we remove the number using `pop()` and try another possibility.

We stop when the combination contains `k` numbers. If its sum is equal to `n`, we add it to the result.

## Algorithm

1. Start from number `1`.
2. Choose a number from `1` to `9`.
3. Add it to the current combination.
4. Continue with the next number so numbers are not reused.
5. If `k` numbers are selected, check their sum.
6. Add the combination if the sum equals `n`.
7. Backtrack and try another combination.

## Time Complexity

**O(C(9, k) × k)**

We explore combinations of `k` numbers selected from the numbers `1` to `9`.

## Space Complexity

**O(k)**

The recursion depth and current combination contain at most `k` elements, excluding the output.

## Key Concepts

- Backtracking
- Recursion
- Combinations
- Arrays
- Pruning

## Author

T.nandhini
