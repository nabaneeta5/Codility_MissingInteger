# Codility_MissingInteger
Find the smallest positive integer that does not occur in a given sequence.

# Task description
Write a function:
that, given an array A of N integers, returns the smallest positive integer (greater than 0) that does not occur in A.

# Link Details
[trainingJFEC8T-DGD](https://app.codility.com/demo/results/trainingJFEC8T-DGD/)

# Programming Language
Java SE 8

# Solution Code

```
import java.util.*;

class Solution {
    public int solution(int[] A) {
        // write your code in Java SE 8
        int N = A.length;
        Set<Integer> set = new HashSet<>();
        for (int a : A) {
            if (a > 0) {
                set.add(a);
            }
        }
        for (int i = 1; i <= N + 1; i++) {
            if (!set.contains(i)) {
                return i;
            }
        }
        return 0;
    }
}

```

