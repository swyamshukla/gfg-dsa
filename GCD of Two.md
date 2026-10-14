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

### Accepted Solutions (3)

#### Solution 1 (Python)

- **Submitted:** 2026-07-16 22:34:45
- **Status:** Correct
- **Marks:** 0

```python
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

#### Solution 2 (Python)

- **Submitted:** 2026-07-16 22:31:12
- **Status:** Correct
- **Marks:** 0

```python
import java.math.*;
class Solution {
    
    public static int gcd(int a, int b) {
        // code here
        BigInteger r =BigInteger.valueOf(a);
        BigInteger p =BigInteger.valueOf(b);
        

        
        return r.gcd(p).intValue();
        
        
    }
}
```

#### Solution 3 (Python)

- **Submitted:** 2026-03-16 22:29:46
- **Status:** Correct
- **Marks:** 1

```python
class Solution {
    
    static int gcdRecursion(int a, int b){
        if(a==0) return b;
        
        return gcdRecursion(b%a,a);

    }
    
    public static int gcd(int a, int b) {
        // code here
        if(a>b){
         return   gcdRecursion(b,a);
        }
        
        return gcdRecursion(a,b);
        
        
    }
}
```

*Generated on: 14/10/2026, 23:53:15*