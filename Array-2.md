# Array-2

## countEvens
```java
public int countEvens(int[] nums) {
  int count = 0;
  
  for(int n: nums) {
    if(n % 2 == 0) count++;
  }
  
  return count;
}
```

## bigDiff
```java
public int bigDiff(int[] nums) {
  int min = nums[0];
  int max = nums[0];
  
  for(int n: nums) {
    min = Math.min(min, n);
    max = Math.max(max, n);
  }
  
  return max - min;
}
```

## centeredAverage
```java
public int centeredAverage(int[] nums) {
  int min = nums[0];
  int max = nums[0];
  int sum = 0;
  
  for(int n: nums) {
    min = Math.min(min, n);
    max = Math.max(max, n);
    sum += n;
  }
  
  return (sum - min - max) / (nums.length - 2);
}
```

## sum13
```java
public int sum13(int[] nums) {
  int sum = 0;
  
  for(int i = 0; i < nums.length; i++) {
    if(nums[i] == 13) {
      i++;
    } else {
      sum += nums[i];
    }
  }
  
  return sum;
}
```

## sum67
```java
public int sum67(int[] nums) {
  boolean doSum = true;
  int sum = 0;
  
  for(int n: nums) {
    if(n == 6) doSum = false;
    if(doSum) sum += n;
    if(n == 7) doSum = true;
  }
  
  return sum;
}
```

## has22
```java
public boolean has22(int[] nums) {
  boolean prev2 = false;
  
  for(int n: nums) {
    if(n == 2) {
      if(prev2) return true;
      prev2 = true;
    } else {
      prev2 = false;
    }
  }
  
  return false;
}
```

## lucky13
```java
public boolean lucky13(int[] nums) {
  boolean contains1 = false;
  boolean contains3 = false;
  
  for(int n: nums) {
    if(n == 1) contains1 = true;
    if(n == 3) contains3 = true;
    if(contains1 || contains3) return false;
  }
  
  return true;
}
```

## sum28
```java
public boolean sum28(int[] nums) {
  int sum = 0;
  
  for(int n: nums) {
    if(n == 2) sum += n;
  }
  
  return sum == 8;
}
```

## more14
```java
public boolean more14(int[] nums) {
  int count1s = 0;
  int count4s = 0;
  
  for(int n: nums) {
    if(n == 1) count1s++;
    if(n == 4) count4s++;
  }
  
  return count1s > count4s;
}
```

## fizzArray
```java
public int[] fizzArray(int n) {
  int[] nums = new int[n];
  
  for(int i = 0; i < n; i++) {
    nums[i] = i;
  }
  
  return nums;
}
```

## only14
```java
public boolean only14(int[] nums) {
  for(int n: nums) {
    if(n != 1 && n != 4) return false;
  }
  
  return true;
}
```

## fizzArray2
```java
public String[] fizzArray2(int n) {
  String[] nums = new String[n];
  
  for(int i = 0; i < n; i++) {
    nums[i] = String.valueOf(i);
  }
  
  return nums;
}
```

## no14
```java
public boolean no14(int[] nums) {
  boolean contains1s = false;
  boolean contains4s = false;
  
  for(int n: nums) {
    if(n == 1) contains1s = true;
    if(n == 4) contains4s = true;
  }
  
  return !(contains1s && contains4s);
}
```

## isEverywhere
```java
public boolean isEverywhere(int[] nums, int val) {
  if(nums.length <= 1) return true;
  
  for(int i = 0; i < nums.length - 1; i++) {
    if(!(nums[i] == val || nums[i+1] == val)) return false;
  }
  
  return true;
}
```

## either24
```java
public boolean either24(int[] nums) {
  boolean one2 = false;
  boolean two2 = false;
  boolean one4 = false;
  boolean two4 = false;
  
  for(int n: nums) {
    switch (n) {
      case 2:
        two2 = one2 ? true : false;
        one2 = true;
        break;
      case 4:
        two4 = one4 ? true : false;
        one4 = true;
        break;
      default:
        one2 = false;
        one4 = false;
    }
  }
  
  return two2 ^ two4;
}
```

## matchUp
```java
public int matchUp(int[] nums1, int[] nums2) {
  int count = 0;
  
  for(int i = 0; i < nums1.length; i++) {
    int n1 = nums1[i];
    int n2 = nums2[i];
    if(Math.abs(n1 - n2) <= 2 && Math.abs(n1 - n2) > 0) count++;
  }
  
  return count;
}
```

## has77
```java
public boolean has77(int[] nums) {
  int indexOfSeven = -1;
  
  for(int i = 0; i < nums.length; i++) {
    int n = nums[i];
    if(n == 7) {
      if(indexOfSeven != -1 && i - indexOfSeven <= 2) {
        return true;
      } else {
        indexOfSeven = i;
      }
    }
  }
  
  return false;
}
```

## has12
```java

```