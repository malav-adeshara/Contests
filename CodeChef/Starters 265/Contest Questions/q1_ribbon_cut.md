# Question 1: Ribbon Cut

## Problem Statement

You have a ribbon of length $N$. You want to cut it into two pieces of positive integer lengths such that one piece is exactly twice as long as the other.

Determine whether this is possible.

## Input Format

The only line of input contains a single integer $N$.

## Output Format

Output `YES` if it is possible, and `NO` otherwise.

Each letter of `YES` and `NO` may be printed in either uppercase or lowercase.

## Constraints

- $1 \le N \le 20$

## Sample 1

**Input**
```
6
```

**Output**
```
YES
```

**Explanation:** Cut the ribbon into pieces of lengths $2$ and $4$.

## Sample 2

**Input**
```
10
```

**Output**
```
NO
```

**Explanation:** The possible size pairs after cutting are: $(1,9), (2,8), (3,7), (4,6), (5,5)$. It can be verified that none of them work.

## Sample 3

**Input**
```
9
```

**Output**
```
YES
```

## Limits

| Time limit | Memory limit | Source limit |
|------------|--------------|--------------|
| 1 sec      | 1.5 GB       | 50000 Bytes  |
