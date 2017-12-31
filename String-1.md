# String-1

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

## middleThree
```java
public String middleThree(String str) {
  int middle = str.length() / 2;
  if(str.length() > 3) return str.substring(middle - 1, middle + 2);
  return str;
}
```

## hasBad
```java
public boolean hasBad(String str) {
  if(str.length() >= 4 && str.substring(1, 4).equals("bad")) return true;
  if(str.length() >= 3 && str.substring(0, 3).equals("bad")) return true;
  return false;
}
```

## atFirst
```java
public String atFirst(String str) {
  if(str.length() == 1) return "" + str.charAt(0) + "@";
  if(str.length() == 0) return "@@";
  return str.substring(0, 2);
}
```

## lastChars
```java
public String lastChars(String a, String b) {
  char firstOfa = a.length() > 0 ? a.charAt(0) : '@';
  char lastOfb = b.length() > 0 ? b.charAt(b.length() - 1) : '@';
  return "" + firstOfa + lastOfb;
}
```

## conCat
```java
public String conCat(String a, String b) {
  if(a.length() > 0 && b.length() > 0 &&
    a.charAt(a.length() - 1) == b.charAt(0)) {
      b = b.substring(1, b.length());
    }
    return a + b;
}
```

## lastTwo
```java
public String lastTwo(String str) {
  int len = str.length();
  if(len > 1) {
    str = str.substring(0, len - 2) + str.charAt(len - 1) + str.charAt(len - 2);
  }
  return str;
}
```

## seeColor
```java
public String seeColor(String str) {
  if(str.startsWith("red")) return "red";
  if(str.startsWith("blue")) return "blue";
  return "";
}
```

## frontAgain
```java
public boolean frontAgain(String str) {
  int len = str.length();
  if(len >= 2) return (str.substring(0, 2).equals(str.substring(len - 2, len)));
  return false;
}
```

## minCat
```java
public String minCat(String a, String b) {
  int lenA = a.length();
  int lenB = b.length();
  if(lenA > lenB) a = a.substring(lenA - lenB);
  if(lenA < lenB) b = b.substring(lenB - lenA);
  return a + b;
}
```

## extraFront
```java
public String extraFront(String str) {
  if(str.length() > 2) str = str.substring(0, 2);
  return str + str + str;
}
```

## without2
```java
public String without2(String str) {
  int len = str.length();
  if(len < 2) return str;
  if(str.substring(0, 2).equals(str.substring(len - 2))) {
    str = str.substring(2);
  }
  return str;
}
```

## deFront
```java
public String deFront(String str) {    
  String firstChar = str.substring(0, 1);
  String secondChar = str.substring(1, 2);
  String endOfStr = str.substring(2);
  
  if(!firstChar.equals("a")) firstChar = "";
  if(!secondChar.equals("b")) secondChar = "";
  
  return firstChar + secondChar + endOfStr;
}
```

## startWord
```java
public String startWord(String str, String word) {
  if(str.length() > 0) {
    char firstChar = str.charAt(0);
    String subStr = str.substring(1);
    String subWord = word.substring(1);
    if(subStr.startsWith(subWord)) return "" + firstChar + subWord;
  }
  return "";
}
```

## withoutX
```java
public String withoutX(String str) {
  if(str.startsWith("x")) str = str.substring(1);
  if(str.endsWith("x")) str = str.substring(0, str.length() - 1);
  return str;
}
```

## withoutX2
```java
public String withoutX2(String str) {
  if(str.isEmpty()) return "";
  if(str.substring(1).startsWith("x")) str = "" + str.charAt(0) + str.substring(2);
  if(str.startsWith("x")) str = str.substring(1);
  return str;
}
```