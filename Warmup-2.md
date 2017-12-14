# Warmup-2

## stringTimes
```java
public String stringTimes(String str, int n) {
  String res = "";
  for(int i = 0; i < n; i++) res = res + str;
  return res;
}
```

## frontTimes
```java
public String frontTimes(String str, int n) {
  String res = "";
  if(str.length() >= 3) str = str.substring(0, 3);
  for(int i = 0; i < n; i++) res = res + str;
  return res;
}
```

## countXX
```java
int countXX(String str) {
  int count = 0;
  for(int i = 0; i < str.length() -1; i++) {
    if(str.charAt(i) == 'x' && str.charAt(i + 1) == 'x') count++;
  }
  return count;
}
```

## doubleX
```java
boolean doubleX(String str) {
  for(int i = 0; i < str.length() - 1; i++) {
    if(str.charAt(i) == 'x') {
      if(str.charAt(i + 1) == 'x') return true;
      return false;
    }
  }
  return false;
}
```

## stringBits
```java
public String stringBits(String str) {
  String res = "";
  for(int i = 0; i < str.length(); i+=2) res = res + str.charAt(i);
  return res;
}
```

## stringSplosion
```java
public String stringSplosion(String str) {
  String res = "";
  String subStr = "";
  for(char ch: str.toCharArray()) {
    subStr = subStr + ch;
    res = res + subStr;
  }
  return res;
}
```

## last2
```java

```