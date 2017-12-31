# Logic-2

## makeBricks
```java
public boolean makeBricks(int small, int big, int goal) {
  goal = goal / 5 <= big ? goal % 5 : goal - 5 * big;
  return goal <= small;
}
```

## loneSum
```java
public int loneSum(int a, int b, int c) {
  if(a == b && b == c) return 0;
  if(a == b) return c;
  if(b == c) return a;
  if(a == c) return b;
  return a + b + c;
}
```

## luckySum
```java
public int luckySum(int a, int b, int c) {
  if(a == 13) return 0;
  if(b == 13) return a;
  if(c == 13) return a + b;
  return a + b + c;
}
```

## noTeenSum
```java
public int noTeenSum(int a, int b, int c) {
  return fixTeen(a) + fixTeen(b) + fixTeen(c);
}

public int fixTeen(int n) {
  if(n == 15 || n == 16) return n;
  return (n >= 13 && n <= 19) ? 0 : n;
}
```

## roundSum
```java
public int roundSum(int a, int b, int c) {
  return round10(a) + round10(b) + round10(c);
}

public int round10(int num) {
  return (num % 10 >= 5) ? (num / 10 + 1) * 10 : (num / 10) * 10;
}
```

## closeFar
```java
public boolean closeFar(int a, int b, int c) {
  return Math.abs(b - c) >= 2 &&
    (
      (Math.abs(a - b) <= 1 && Math.abs(a - c) >= 2) ||
      (Math.abs(a - c) <= 1 && Math.abs(a - b) >= 2)
    );
}
```

## blackjack
```java
public int blackjack(int a, int b) {
  a = a > 21 ? 0 : a;
  b = b > 21 ? 0 : b;
  return Math.max(a, b);
}
```

## evenlySpaced
```java
public boolean evenlySpaced(int a, int b, int c) {
  int[] nums = new int[] {a, b, c};
  Arrays.sort(nums);
  return nums[1] - nums[0] == nums[2] - nums[1];
}
```

## makeChocolate
```java
public int makeChocolate(int small, int big, int goal) {
  if(goal - 5 * big > small) return -1;
  while(big-- > 0 && goal >= 5) {
    goal -= 5;
  }
  return goal <= small ? goal : -1;
}
```