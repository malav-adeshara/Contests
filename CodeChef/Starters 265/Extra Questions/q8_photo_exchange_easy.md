# Practice Question 1: Photo Exchange (Easy)

> This is the easy version of the problem. In this version, $Q = N$, every person is asked about exactly once, and all queries have the same time. The two versions are otherwise identical.

## Problem Statement

There are $N$ people on a number line. Person $i$ starts at position $X_i$, where $X_1 < X_2 < \ldots < X_N$, and moves with constant velocity $V_i$ (which may be negative or zero).

Initially, person $i$ has only photograph $i$. Whenever two (or more) people meet at the same point at the same moment, they share their photographs; and each of them ends up with every photograph that any of them had. People pass through each other without changing velocity.

You are given $Q$ queries. Each query gives a time $K$ and a person $P$, and you must report the number of distinct photographs person $P$ has at time $K$. This includes exchanges that happen exactly at time $K$.

In this version of the problem, all queries have the same value of $K$, and each person appears exactly once.

## Input Format

- The first line of input will contain a single integer $T$, denoting the number of test cases.
- Each test case consists of multiple lines of input.
  - The first line of each test case contains two space-separated integers $N$ and $Q$ — the number of people and the number of queries.
  - The second line contains $N$ space-separated integers $X_1, X_2, \ldots, X_N$ — the starting positions.
  - The third line contains $N$ space-separated integers $V_1, V_2, \ldots, V_N$ — the velocities.
  - The next $Q$ lines describe the queries. The $j$-th of these lines contains two space-separated integers $K_j$ and $P_j$ — the time and the person of the $j$-th query.

## Output Format

For each query, output on a new line the number of distinct photographs person $P_j$ has at time $K_j$.

## Constraints

- $1 \le T \le 10^5$
- $3 \le N \le 2 \cdot 10^5$
- $Q = N$
- $-10^9 \le X_i, V_i \le 10^9$
- $X_1 < X_2 < \ldots < X_N$
- $1 \le K_j \le 10^9$
- $1 \le P_j \le N$
- All $K_j$ are equal.
- $P_i \ne P_j$ for $i \ne j$.
- The sum of $N$ over all test cases does not exceed $2 \cdot 10^5$.

## Sample 1

**Input**
```
4
3 3
0 2 6
4 2 0
1 3
1 1
1 2
4 4
1 2 3 4
4 3 2 1
1 2
1 4
1 1
1 3
5 5
-7 -1 1 7 12
6 8 9 4 2
4 4
4 1
4 5
4 3
4 2
3 3
-1000000000 1 900000000
1000000000 999999999 999999999
1000000000 2
1000000000 3
1000000000 1
```

**Output**
```
1
2
2
4
4
4
4
4
1
4
3
4
1
1
1
```

**Explanation:**

- **Test case 1:** Persons $1$ and $2$ meet at position $4$ at time $1$, so both have $2$ photographs. Person $3$ stays at position $6$ and meets nobody.
- **Test case 4:** Nobody ever meets. Person $1$ catches up with person $2$ by one unit per unit of time, but at time $K$ is still one unit behind: at positions $10^{18} - 10^9$ and $10^{18} - 10^9 + 1$. Persons $2$ and $3$ have the same velocity.

## Limits

| Time limit | Memory limit | Source limit |
|------------|--------------|--------------|
| 2 secs     | 1.5 GB       | 50000 Bytes  |
