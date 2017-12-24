## firstLast6
```java
public boolean firstLast6(int[] nums) {
  return (nums[0] == 6 || nums[nums.length-1] == 6);
}
```

## sameFirstLast
```java
public boolean sameFirstLast(int[] nums) {
  return (nums.length >= 1 && nums[0] == nums[nums.length-1]);
}
```

## makePi
```java
public int[] makePi() {
  return new int[] {3, 1, 4};
}
```

## commonEnd
```java
public boolean commonEnd(int[] a, int[] b) {
  return (a[0] == b[0] || a[a.length-1] == b[b.length-1]);
}
```

## sum3
```java
public int sum3(int[] nums) {
  return nums[0] + nums[1] + nums[2];
}
```

## rotateLeft3
```java
public int[] rotateLeft3(int[] nums) {
  return new int[] {nums[1], nums[2], nums[0]};
}
```

## reverse3
```java
public int[] reverse3(int[] nums) {
  return new int[] {nums[2], nums[1], nums[0]};
}
```

## maxEnd3
```java
public int[] maxEnd3(int[] nums) {
  int max = nums[0];
  if(nums[2] > max) max = nums[2];
  return new int[] {max, max, max};
}
```

## sum2
```java
public int sum2(int[] nums) {
  if(nums.length == 0) return 0;
  if(nums.length == 1) return nums[0];
  return nums[0] + nums[1];
}
```

## middleWay
```java
public int[] middleWay(int[] a, int[] b) {
  return new int[] {a[1], b[1]};
}
```

## makeEnds
```java
public int[] makeEnds(int[] nums) {
  return new int[] {nums[0], nums[nums.length-1]};
}
```

## has23
```java
public boolean has23(int[] nums) {
  return nums[0] == 2 || nums[0] == 3 || nums[1] == 2 || nums[1] == 3;
}
```

## no23
```java
public boolean no23(int[] nums) {
  return !(nums[0] == 2 || nums[0] == 3 || nums[1] == 2 || nums[1] == 3);
}
```

## makeLast
```java
public int[] makeLast(int[] nums) {
  int[] newNums = new int[nums.length * 2];
  newNums[newNums.length-1] = nums[nums.length-1];
  return newNums;
}
```

## double23
```java
public boolean double23(int[] nums) {
  if(nums.length == 2) return nums[0] == 2 && nums[1] == 2 ||
                              nums[0] == 3 && nums[1] == 3;
  return false;
}
```

## fix23
```java
public int[] fix23(int[] nums) {
  if(nums[0] == 2 && nums[1] == 3) nums[1] = 0;
  if(nums[1] == 2 && nums[2] == 3) nums[2] = 0;
  return nums;
}
```

## start1
```java
public int start1(int[] a, int[] b) {
  int count = 0;
  if(a.length > 0 && a[0] == 1) count++;
  if(b.length > 0 && b[0] == 1) count++;
  return count;
}
```

## biggerTwo
```java
public int[] biggerTwo(int[] a, int[] b) {
  if((a[0] + a[1]) >= (b[0] + b[1])) {
    return a;
  } else {
    return b;
  }
}
```

## makeMiddle
```java
public int[] makeMiddle(int[] nums) {
  int len = nums.length;
  return new int[] {nums[len/2 - 1], nums[len/2]};
}
```

## plusTwo
```java
public int[] plusTwo(int[] a, int[] b) {
  return new int[] {a[0], a[1], b[0], b[1]};
}
```

## swapEnds
```java
public int[] swapEnds(int[] nums) {
  int len =  nums.length;
  
  if(len < 2) return nums;
  
  int tmp = nums[0];
  nums[0] = nums[len-1];
  nums[len-1] = tmp;
  return nums;
}
```

## midThree
```java
public int[] midThree(int[] nums) {
  int len = nums.length;
  return new int[] {nums[len/2 - 1], nums[len/2], nums[len/2 + 1]};
}
```

## maxTriple
```java
public int maxTriple(int[] nums) {
  int len = nums.length;
  int max = nums[0];
  
  if(len > 1) {
    int maxOfMiddleAndLast = Math.max(nums[len/2], nums[len - 1]);
    max = max > maxOfMiddleAndLast ? max : maxOfMiddleAndLast;
  }
  
  return max;
}
```

## frontPiece
```java
public int[] frontPiece(int[] nums) {
  if(nums.length < 2) return nums;
  return new int[] {nums[0], nums[1]};
}
```

## unlucky1
```java
public boolean unlucky1(int[] nums) {
  if(nums.length < 2) return false;
  return (nums[0] == 1 && nums[1] == 3 ||
          nums[1] == 1 && nums[2] == 3 ||
          nums[nums.length - 2] == 1 && nums[nums.length - 1] == 3);
}
```

## make2
```java
public int[] make2(int[] a, int[] b) {
  if(a.length == 0) return new int[] {b[0], b[1]};
  if(a.length == 1) return new int[] {a[0], b[0]};
  return new int[] {a[0], a[1]}; 
}
```

## front11
```java
public int[] front11(int[] a, int[] b) {
  if(a.length == 0 && b.length == 0) return a;
  if(a.length == 0) return new int[] {b[0]};
  if(b.length == 0) return new int[] {a[0]};
  return new int[] {a[0], b[0]};
}
```