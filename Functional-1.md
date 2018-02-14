# Functional-1

## doubling
```java
public List<Integer> doubling(List<Integer> nums) {
  return nums.stream()
    .map(n -> n * 2)
    .collect(Collectors.toList());
}
```

## square
```java
public List<Integer> square(List<Integer> nums) {
  return nums
    .stream()
    .map(n -> n * n)
    .collect(Collectors.toList());
}
```

## addStar
```java
public List<String> addStar(List<String> strings) {
  return strings
    .stream()
    .map(s -> s + "*")
    .collect(Collectors.toList());
}
```

## copies3
```java
public List<String> copies3(List<String> strings) {
  return strings
    .stream()
    .map(s -> s + s + s)
    .collect(Collectors.toList());
}
```

## moreY
```java
public List<String> moreY(List<String> strings) {
  return strings
    .stream()
    .map(s -> "y" + s + "y")
    .collect(Collectors.toList());
}
```

## math1
```java
public List<Integer> math1(List<Integer> nums) {
  return nums
    .stream()
    .map(n -> (n + 1) * 10)
    .collect(Collectors.toList());
}
```

## rightDigit
```java
public List<Integer> rightDigit(List<Integer> nums) {
  return nums
    .stream()
    .map(n -> n % 10)
    .collect(Collectors.toList());
}
```

## lower
```java
public List<String> lower(List<String> strings) {
  return strings
    .stream()
    .map(s -> s = s.toLowerCase())
    .collect(Collectors.toList());
}
```

## noX
```java
public List<String> noX(List<String> strings) {
  return strings
    .stream()
    .map(s -> s.replaceAll("x", ""))
    .collect(Collectors.toList());
}
```