## helloName
```java
public String helloName(String name) {
  return "Hello " + name + "!";
}
```

## makeAbba
```java
public String makeAbba(String a, String b) {
  return a + b + b + a;
}
```

## makeTags
```java
public String makeTags(String tag, String word) {
  return "<" + tag + ">" + word + "</" + tag + ">";
}
```

## makeOutWord
```java
public String makeOutWord(String out, String word) {
  return out.substring(0, out.length() / 2) +
    word +
    out.substring(out.length() / 2, out. length());
}
```

## extraEnd
```java
public String extraEnd(String str) {
  int len = str.length();
  return str.substring(len -2, len) +
    str.substring(len -2, len) +
    str.substring(len -2, len);
}
```

## firstTwo
```java
public String firstTwo(String str) {
  if(str.length() > 2) return str.substring(0, 2);
  return str;
}
```

## firstHalf
```java
public String firstHalf(String str) {
  return str.substring(0, str.length() / 2);
}
```

## withoutEnd
```java
public String withoutEnd(String str) {
  return str.substring(1, str.length() - 1);
}
```

## comboString
```java
public String comboString(String a, String b) {
  String shortString = a.length() < b.length() ? a : b;
  String longString = a.length() > b.length() ? a : b;
  
  return shortString + longString + shortString;
}
```

## nonStart
```java
public String nonStart(String a, String b) {
  return a.substring(1, a.length()) + b.substring(1, b.length());
}
```

## left2
```java
public String left2(String str) {
  return str.substring(2, str.length()) + str.substring(0, 2);
}
```

## right2
```java
public String right2(String str) {
  int len = str.length();
  return str.substring(len - 2, len) + str.substring(0, len - 2);
}
```

## theEnd
```java
public String theEnd(String str, boolean front) {
  if(front) return "" + str.charAt(0);
  return "" + str.charAt(str.length() - 1);
}
```

## withouEnd2
```java
public String withouEnd2(String str) {
  if(str.length() > 2) return str.substring(1, str.length() - 1);
  return "";
}
```

## middleTwo
```java
public String middleTwo(String str) {
  int len = str.length() / 2;
  return str.substring(len - 1, len + 1);
}
```

## endsLy
```java
public boolean endsLy(String str) {
  return str.endsWith("ly");
}
```

## nTwice
```java
public String nTwice(String str, int n) {
  return str.substring(0, n) + str.substring(str.length() - n, str.length());
}
```

## twoChar
```java
public String twoChar(String str, int index) {
  if(str.length() - index < 2 || index < 0) return str.substring(0, 2);
  return str.substring(index, index + 2);
}
```