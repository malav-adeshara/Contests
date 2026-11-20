# Question 7: Mixing Valves

## Problem Statement

There are $N$ beakers in a row, numbered $1$ to $N$. Initially, beaker $i$ contains only chemical $i$.

For each $1 \le i < N$, there is a valve between beakers $i$ and $i+1$. This is called valve $i$. Initially, all the valves are closed.

Every valve must be opened **exactly once**, one at a time, in some order. When a valve is opened, the two beakers it connects mix: this causes both beakers to contain every chemical that either of them contained. Then, the valve is closed (so the two beakers can never affect each other again).

You are given the final contents of every beaker. Determine whether some order of opening the valves produces exactly these contents.

If such an order exists, also find any valid order.

## Input Format

- The first line of input will contain a single integer $T$, denoting the number of test cases.
- Each test case consists of multiple lines of input.
  - The first line of each test case contains a single integer $N$ — the number of beakers.
  - The next $N$ lines describe the final contents. The $i$-th of these lines contains a binary string $S_i$ of length $N$, whose $j$-th character is `1` if beaker $i$ contains chemical $j$ at the end, and `0` otherwise.

## Output Format

For each test case:

- If no order of opening the valves produces these contents, output `NO`.
- Otherwise, output `YES` on one line, and on the next line $N-1$ space-separated integers — a permutation of $1, 2, \ldots, N-1$ listing the valves in the order they are opened, where valve $i$ connects beakers $i$ and $i+1$.

If there are multiple valid orders, you may output any of them. Each letter of `YES` and `NO` may be printed in either uppercase or lowercase.

## Constraints

- $1 \le T \le 10^5$
- $3 \le N \le 2000$
- $S_i$ is a binary string of length $N$.
- The sum of $N^2$ over all test cases does not exceed $2000^2$.

## Sample 1

**Input**
```
5
3
110
111
111
5
11100
11100
01111
01111
00011
5
11111
11111
01110
00111
00011
6
111110
111110
011110
001110
000111
000111
6
111111
111111
011111
001111
000101
000011
```

**Output**
```
YES
1 2
YES
2 1 4 3
NO
YES
4 3 2 1 5
NO
```

**Explanation:**

- **Test case 1:** Opening valve $1$ gives beakers $1$ and $2$ the chemicals $\{1, 2\}$. Opening valve $2$ then gives beakers $2$ and $3$ the chemicals $\{1, 2, 3\}$, while beaker $1$ still contains only $\{1, 2\}$. This is where we wanted to end up.
- **Test case 3:** Beaker $1$ contains chemical $5$, and the only way for that to happen is for chemical $5$ to pass through beakers $4, 3, 2$ on the way. This contradicts the fact that beaker $3$ must not contain chemical $5$, so no solution exists.

## Limits

| Time limit | Memory limit | Source limit |
|------------|--------------|--------------|
| 1 sec      | 1.5 GB       | 50000 Bytes  |
