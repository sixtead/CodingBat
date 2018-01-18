# Array-3

## maxSpan
```java
public int maxSpan(int[] nums) {
  int len = nums.length;
  
  if(len < 2) return len;

  return nums[0] == nums[len-1] ? len : len - 1;
}
```

## fix34
```java
public int[] fix34(int[] nums) {
  
  for(int i = 0; i < nums.length; i++) {
    if(nums[i] == 3) {
      for(int j = 0; j < nums.length; j++) {
        if(nums[j] == 4 && nums[j-1] != 3) {
          int tmp = nums[i+1];
          nums[i+1] = nums[j];
          nums[j] = tmp;
          break;
        }
      }
    }
  }
  
  return nums;
}
```

## fix45
```java
public int[] fix45(int[] nums) {
    
  for(int i = 0; i < nums.length; i++) {
    if(nums[i] == 4) {
      for(int j = 0; j < nums.length; j++) {
        if(nums[j] == 5 && (j == 0 || nums[j-1] != 4)) {
          int tmp = nums[i+1];
          nums[i+1] = nums[j];
          nums[j] = tmp;
          break;
        }
      }
    }
  }
  
  return nums;
}
```

## canBalance
```java
public boolean canBalance(int[] nums) {
  int sum = 0;
  int leftSum = 0;
  int i = 0;
  
  for(int n: nums) {
    sum += n;
  }
  
  if(sum % 2 != 0) return false;
  
  while(leftSum <= sum / 2 && i < nums.length) {
    leftSum += nums[i++];
    if(leftSum == sum / 2) return true;
  }
  
  return false;
}
```

## linearIn
```java
public boolean linearIn(int[] outer, int[] inner) {
  int lastIndex = 0;
  
  for(int i = 0; i < inner.length; i++) {
    for(int j = lastIndex; j < outer.length; j++) {
      if(inner[i] != outer[j] && j == outer.length - 1) return false;
      if(i != inner.length - 1 && j == outer.length - 1) return false;
      if(inner[i] == outer[j]) {
        lastIndex = j+1;
        break;
      }
    }
  }
  
  return true;
}
```

## squareUp
```java
public int[] squareUp(int n) {
  int[] nums = new int[n*n];
    
  for(int i = n-1; i >= 0; i--) {
    for(int j = n-i-1; j < n; j++) {
      nums[n*i + j] = n-j;
    }
  }
  
  return nums;
}
```

## seriesUp
```java
public int[] seriesUp(int n) {
  int index = 0;
  int[] nums = new int[n*(n+1)/2];
  
  for(int i = 0; i < n; i++) {
    for(int j = 0; j <= i; j++) {
      nums[index++] = j + 1;
    }
  }
  
  return nums;
}
```

## maxMirror
```java
public int maxMirror(int[] nums) {
  int count = 0;
  int maxCount = 0;
  boolean matchFound = false;

  for(int i = 0; i < nums.length; i++) {
    matchFound = false;
    for(int j = nums.length - 1; j >= 0; j--) {
      if(count == 0 && nums[i] == nums[j]) {
        if(!matchFound) {
          count = 1;
          matchFound = true;
        }
      } else if(i > 0 && j < nums.length - 1
                && nums[i] == nums[j] && nums[i-1] == nums[j+1]) {
          if(!matchFound) {
            count++;
            matchFound = true;
          }
      }
    }
    maxCount = Math.max(maxCount, count);
    if(!matchFound) {
      count = 0;
      i--;
    }
  }
  return maxCount;
}
```

## countClumps
```java
public int countClumps(int[] nums) {
  int count = 0;
  int clumps = 0;
  
  for(int i = 1; i < nums.length; i++) {
    if(nums[i] == nums[i-1]) {
      count++;
    } else {
      clumps = count > 0 ? clumps + 1 : clumps;
      count = 0;
    }
  }
  clumps = count > 0 ? clumps + 1 : clumps;
  
  return clumps;
}
```