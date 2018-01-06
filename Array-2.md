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
public boolean has12(int[] nums) {
  boolean thereIsOne = false;
  
  for(int n: nums) {
    if(n == 2 && thereIsOne) return true;
    if(n == 1) thereIsOne = true;
  }
  
  return false;
}
```

## modThree
```java
public boolean modThree(int[] nums) {
  int countOdd = 0;
  int countEven = 0;
  
  for(int n: nums) {
    if(n % 2 != 0) {
      countOdd++;
      countEven = 0;
    }
    if(n % 2 == 0) {
      countEven++;
      countOdd = 0;
    }
    if(countOdd == 3 || countEven == 3) return true;
  }
  
  return false;
}
```

## haveThree
```java
public boolean haveThree(int[] nums) {
  int count = 0;
  boolean prevThree = false;
  
  for(int n: nums) {
    if(n == 3) {
      if(prevThree) return false;
      prevThree = true;
      count++;
    } else {
      prevThree = false;
    }
  }
  
  return count == 3;
}
```

## twoTwo
```java
public boolean twoTwo(int[] nums) {
  boolean firstTwo = false;
  boolean secondTwo = true;
  
  for(int n: nums) {
    if(n == 2) {
      secondTwo = firstTwo ? true : false;
      firstTwo = true;
    } else {
      firstTwo = false;
    }
  }
  
  return secondTwo;
}
```

## sameEnds
```java
public boolean sameEnds(int[] nums, int len) {
  return Arrays.equals(Arrays.copyOfRange(nums, 0, len),
    Arrays.copyOfRange(nums, nums.length - len, nums.length));
}
```

## tripleUp
```java
public boolean tripleUp(int[] nums) {
  int count = 1;
  
  for(int i = 1; i < nums.length; i++) {
    count = (nums[i] - nums[i-1] == 1) ? count + 1 : 1;
    if(count == 3) return true;
  }
  
  return false;
}
```

## fizzArray3
```java
public int[] fizzArray3(int start, int end) {
  int[] nums = new int[end-start];
  
  for(int i = 0; i < end-start; i++) {
    nums[i] = start + i;
  }
  
  return nums;
}
```

## shiftLeft
```java
public int[] shiftLeft(int[] nums) {
  int[] returnArray;
  
  if(nums.length > 0) {
    int[] firstPartOfNums = Arrays.copyOfRange(nums, 1, nums.length);
    returnArray = Arrays.copyOf(firstPartOfNums, nums.length);
    returnArray[nums.length - 1] = nums[0];
  } else {
    returnArray = new int[0];
  }
  
  return returnArray;
}
```

## tenRun
```java
public int[] tenRun(int[] nums) {
  boolean multipleOfTen = false;
  int replace = 0;
  for(int i = 0; i < nums.length; i++) {
    if(nums[i] % 10 == 0) {
      multipleOfTen = true;
      replace = nums[i];
    } else {
      nums[i] = multipleOfTen ? replace : nums[i];
    }
  }
  
  return nums;
}
```

## pre4
```java
public int[] pre4(int[] nums) {
  int len = 0;
  
  for(int i = 0; i < nums.length; i++) {
    if(nums[i] == 4) {
      len = i;
      break;
    }
  }
  
  return Arrays.copyOf(nums, len);
}
```

## post4
```java
public int[] post4(int[] nums) {
  int index = 0;
  
  for(int i = 0; i < nums.length; i++) {
    index = nums[i] == 4 ? i : index;
  }
  
  return Arrays.copyOfRange(nums, index + 1, nums.length);
}
```

## notAlone
```java
public int[] notAlone(int[] nums, int val) {
  for(int i = 0; i < nums.length; i++) {
    if(i > 0 && i < nums.length - 1) {
      nums[i] = (nums[i] == val && val != nums[i-1] && val != nums[i+1])
        ? Math.max(nums[i-1], nums[i+1])
        : nums[i];
    }
  }
  
  return nums;
}
```

## zeroFront
```java

```