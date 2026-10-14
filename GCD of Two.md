## 01. GCD of Two

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/gcd-of-two-numbers3459/1)

### Problem Description

**Task:** Given two positive integers a and b, find GCD of a and b.

> **Note:** Don't use the inbuilt gcd function

#### Examples

##### Example 1

- **Input:**
```text
a = 20, b = 28
```
- **Output:**
```text
4
```
- **Explanation:** GCD of 20 and 28 is 4

##### Example 2

- **Input:**
```text
a = 60, b = 36
```
- **Output:**
```text
12
```
- **Explanation:** GCD of 60 and 36 is 12

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log(min(a, b)))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (5)

#### Solution 1 (Java)

- **Submitted:** 2026-10-14 23:59:41
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public static int gcd(int a, int b) {
        // code here
        if(a>b) return Solution.recursion(a,b);
        return Solution.recursion(b,a);
        
    }
    static int recursion(int a,int b){
        if(a==0) return b;
        return recursion(b%a,a);
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-14 23:39:48
- **Status:** Correct
- **Marks:** 0

```java
import math
class Solution:
    def gcd(self, a, b):
        # code here
        return math.gcd(a,b);
```

#### Solution 3 (Java)

- **Submitted:** 2026-10-14 23:37:27
- **Status:** Correct
- **Marks:** 0

```java
import math
class Solution:
    def gcd(self, a, b):
        # code here
        return math.gcd(a,b);
```

#### Solution 4 (Java)

- **Submitted:** 2026-07-19 01:21:34
- **Status:** Correct
- **Marks:** 0

```java
import java.math.*;

class Solution {
    public static int gcd(int a, int b) {
        // code here
        // if(a<=b){
        BigInteger big = BigInteger.valueOf(a);
      
        
    
        BigInteger ans = big.gcd(BigInteger.valueOf(b));    
    
        return ans.intValue();
    }
}
```

#### Solution 5 (Java)

- **Submitted:** 2026-07-16 22:34:45
- **Status:** Correct
- **Marks:** 0

```java
import java.math.*;
class Solution {
    
    
    static int recursion(int a ,int b){
        if(a==0) return b;
        
        
        return recursion(b%a,a);
        
        
    }
    public static int gcd(int a, int b) {
        // code here
        if(a>b) return recursion(b,a);
        
        return recursion(a,b);
        
        
    }
}
```

*Generated on: 15/10/2026, 00:01:01*