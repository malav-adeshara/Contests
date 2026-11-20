# Question 3: Squash

## Problem Statement

You are given a string $S$ of length $N$ consisting only of the characters `A` and `B`, and an integer $K$.

In one operation, you may choose two adjacent equal characters of $S$ and delete exactly one of them.

Determine whether it is possible to obtain a string of length exactly $K$ after performing zero or more operations.

## Input Format

- The first line of input will contain a single integer $T$, denoting the number of test cases.
- Each test case consists of two lines of input.
  - The first line of each test case contains two space-separated integers $N$ and $K$.
  - The second line contains the string $S$.

## Output Format

For each test case, output on a new line `YES` if a string of length $K$ can be obtained, and `NO` otherwise.

Each letter of `YES` and `NO` may be printed in either uppercase or lowercase.

## Constraints

- $1 \le T \le 100$
- $1 \le K \le N \le 100$
- $S$ consists only of the characters `A` and `B`.

## Sample 1

**Input**
```
5
10 3
BBBAAAAAAB
4 3
ABAB
5 1
AAAAA
6 6
ABBAAB
9 4
ABBBAABAA
```

**Output**
```
YES
NO
YES
YES
NO
```

**Explanation:**

- **Test case 1:** `BBBAAAAAAB` can be reduced to `BAB`, which has length $3$. One valid sequence is as follows:
  1. Choose one of the first two characters and delete them. The string becomes `BBAAAAAAB`.
  2. Again choose one of the first two characters and delete them. The string becomes `BAAAAAAB`.
  3. Now repeatedly choose two adjacent `A`'s and delete one of them. The string will eventually become `BAB`.
- **Test case 2:** No two adjacent characters of `ABAB` are equal, so no operation can be performed and the length stays $4$.

## Limits

| Time limit | Memory limit | Source limit |
|------------|--------------|--------------|
| 1 sec      | 1.5 GB       | 50000 Bytes  |
