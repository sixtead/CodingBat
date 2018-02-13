# Recursion-2

## groupSum
```java
public boolean groupSum(int start, int[] nums, int target) {
  if(start >= nums.length) return (target == 0);
  if(groupSum(start + 1, nums, target - nums[start])) return true;
  if(groupSum(start + 1, nums, target)) return true;
  return false;
}
```

## groupSum6
```java
public boolean groupSum6(int start, int[] nums, int target) {
  if(start >= nums.length) return target == 0;
  if(nums[start] == 6) return groupSum6(start + 1, nums, target - 6);
  if(groupSum6(start + 1, nums, target - nums[start])) return true;
  if(groupSum6(start + 1, nums, target)) return true;
  return false;
}
```

## groupNoAdj
```java
public boolean groupNoAdj(int start, int[] nums, int target) {
  if(start >= nums.length) return target == 0;
  if(groupNoAdj(start + 2, nums, target - nums[start])) return true;
  if(groupNoAdj(start + 1, nums, target)) return true;
  return false;
}
```

## groupSum5
```java
public boolean groupSum5(int start, int[] nums, int target) {
  if(start >= nums.length) return target == 0;
  if(nums[start] % 5 == 0) {
    return start < nums.length - 1 && nums[start+1] == 1
        ? groupSum5(start + 2, nums, target - nums[start])
        : groupSum5(start + 1, nums, target - nums[start]);
  }
  if(groupSum5(start + 1, nums, target - nums[start])) return true;
  if(groupSum5(start + 1, nums, target)) return true;
  return false;
}
```

## groupSumClump
```java
public boolean groupSumClump(int start, int[] nums, int target) {
    if(start >= nums.length) return target == 0;
          
    int i = start;
    int sum = 0;
    
    while(i < nums.length && nums[start] == nums[i]) {
        sum += nums[i];
        i++;
    }
                              
    if(groupSumClump(i, nums, target - sum)) return true;
    if(groupSumClump(i, nums, target)) return true;
    return false;
}
```

## splitArray
```java
public boolean splitArray(int[] nums) {
  return splitEquals(0, nums, 0, 0);
}

public boolean splitEquals(int start, int[] nums, int sum1, int sum2) {
  if(start >= nums.length) return sum1 == sum2;
  if(splitEquals(start + 1, nums, sum1 + nums[start], sum2)) return true;
  return splitEquals(start + 1, nums, sum1, sum2 + nums[start]);
}
```

## splitOdd10
```java
public boolean splitOdd10(int[] nums) {
  return splitSumOdd10(0, nums, 0, 0);
}

public boolean splitSumOdd10(int start, int[] nums, int sum10, int sumOdd) {
  if(start >= nums.length) return sum10 % 10 == 0 && sumOdd % 2 != 0;
  if(splitSumOdd10(start + 1, nums, sum10 + nums[start], sumOdd)) return true;
  return splitSumOdd10(start + 1, nums, sum10, sumOdd + nums[start]);
}
```

## split53
```java
public boolean split53(int[] nums) {
  return splitSum53(0, nums, 0, 0);
}

public boolean splitSum53(int start, int[] nums, int sum5, int sum3) {
  if(start >= nums.length) return sum5 == sum3;
  if(nums[start] % 5 == 0) return splitSum53(start + 1, nums, sum5 + nums[start], sum3);
  if(nums[start] % 3 == 0) return splitSum53(start + 1, nums, sum5, sum3 + nums[start]);
  if(splitSum53(start + 1, nums, sum5 + nums[start], sum3)) return true;
  return splitSum53(start + 1, nums, sum5, sum3 + nums[start]);
}
```