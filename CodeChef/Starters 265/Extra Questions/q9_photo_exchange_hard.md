# Question 2 (Practice): Photo Exchange (Hard)

> This is the hard version of the problem. In this version, the queries have no extra constraints. The two versions are otherwise identical.

## Problem Statement

There are $N$ people on a number line. Person $i$ starts at position $X_i$, where $X_1 < X_2 < \ldots < X_N$, and moves with constant velocity $V_i$ (which may be negative or zero).

Initially, person $i$ has only photograph $i$. Whenever two (or more) people meet at the same point at the same moment, they share their photographs; and each of them ends up with every photograph that any of them had. People pass through each other without changing velocity.

You are given $Q$ queries. Each query gives a time $K$ and a person $P$, and you must report the number of distinct photographs person $P$ has at time $K$. This includes exchanges that happen exactly at time $K$.

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
- $1 \le Q \le 2 \cdot 10^5$
- $-10^9 \le X_i, V_i \le 10^9$
- $X_1 < X_2 < \ldots < X_N$
- $1 \le K_j \le 10^9$
- $1 \le P_j \le N$
- The sum of $N$ over all test cases does not exceed $2 \cdot 10^5$.
- The sum of $Q$ over all test cases does not exceed $2 \cdot 10^5$.

## Sample 1

**Input**
```
4
3 6
0 2 6
4 2 0
1 1
2 3
1 2
3 3
2 1
5 2
5 10
-5 1 7 13 19
-1 5 2 -4 -4
4 2
1 4
2 1
3 3
4 5
1 2
2 4
3 1
4 3
1 5
5 7
-7 -1 1 7 12
6 8 9 4 2
4 1
1 4
2 3
4 5
1 2
3 5
2 2
3 4
-1000000000 1 900000000
1000000000 999999998 999999999
1 1
1000000000 1
1000000000 2
999999999 3
```

**Output**
```
2
3
2
3
3
3
4
2
1
4
4
1
3
1
4
1
1
1
3
4
1
4
3
1
2
2
1
```

**Explanation:**

- **Test case 1:** Persons $1$ and $2$ meet at position $4$ at time $1$. Person $1$ reaches person $3$ at position $6$ at time $1.5$, and person $2$ reaches person $3$ there at time $2$. So, for example, at time $2$ person $1$ has all $3$ photographs.
- **Test case 4:** Persons $1$ and $2$ meet at time $500000000.5$. Person $3$ meets nobody before time $10^9$.

## Limits

| Time limit | Memory limit | Source limit |
|------------|--------------|--------------|
| 3 secs     | 1.5 GB       | 50000 Bytes  |
