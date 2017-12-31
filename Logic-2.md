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

```