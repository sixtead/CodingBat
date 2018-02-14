# Functional-2

## noNeg
```java
public List<Integer> noNeg(List<Integer> nums) {
  return nums
    .stream()
    .filter(n -> n >= 0)
    .collect(Collectors.toList());
}
```

## no9
```java
public List<Integer> no9(List<Integer> nums) {
  return nums
    .stream()
    .filter(n -> n % 10 != 9)
    .collect(Collectors.toList());
}
```

## noTeen
```java
public List<Integer> noTeen(List<Integer> nums) {
  return nums
    .stream()
    .filter(n -> n < 13 || n > 19)
    .collect(Collectors.toList());
}
```

## noLong
```java
public List<String> noLong(List<String> strings) {
  return strings
    .stream()
    .filter(s -> s.length() < 4)
    .collect(Collectors.toList());
}
```

## noZ
```java
public List<String> noZ(List<String> strings) {
  return strings
    .stream()
    .filter(s -> s.indexOf('z') == -1)
    .collect(Collectors.toList());
}
```

## no34
```java
public List<String> no34(List<String> strings) {
  return strings
    .stream()
    .filter(s -> s.length() != 3 && s.length() != 4)
    .collect(Collectors.toList());
}
```

## noYY
```java
public List<String> noYY(List<String> strings) {
  return strings
    .stream()
    .map(s -> s + "y")
        .filter(s -> s.indexOf("yy") == -1)
    .collect(Collectors.toList());
}
```

## two2
```java
public List<Integer> two2(List<Integer> nums) {
  return nums
    .stream()
    .map(n -> n * 2)
    .filter(n -> n % 10 != 2)
    .collect(Collectors.toList());
}
```

## square56
```java
public List<Integer> square56(List<Integer> nums) {
  return nums
    .stream()
    .map(n -> n * n + 10)
    .filter(n -> n % 10 != 5 && n % 10 != 6)
    .collect(Collectors.toList());
}
```