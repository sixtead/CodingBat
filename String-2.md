# String-2

## doubleChar
```java
public String doubleChar(String str) {
  String result = "";
  
  for(char c: str.toCharArray()) {
    result = result + c + c;
  }
  
  return result;
}
```

## countHi
```java
public int countHi(String str) {
  int count = 0;
  
  for(int i = 0; i < str.length(); i++) {
    if(str.startsWith("hi", i)) count++;
  }
  
  return count;
}
```

## catDog
```java
public boolean catDog(String str) {
  int countCat = 0;
  int countDog = 0;
  
  for(int i = 0; i < str.length(); i++) {
    if(str.startsWith("cat", i)) countCat++;
    if(str.startsWith("dog", i)) countDog++;
  }
  
  return countCat == countDog;
}
```

## countCode
```java
public int countCode(String str) {
  int count = 0;
  
  for(int i = 0; i < str.length() - 3; i++) {
    if(str.charAt(i) == 'c' &&
        str.charAt(i+1) == 'o' &&
        str.charAt(i+3) == 'e') {
      count++;
    }
  }
  
  return count;
}
```

## endOther
```java
public boolean endOther(String a, String b) {
  a = a.toLowerCase();
  b = b.toLowerCase();
  
  return a.endsWith(b) || b.endsWith(a);
}
```

## xyzThere
```java
public boolean xyzThere(String str) {
  int countFalse = 0;
  int countTrue = 0;
  
  for(int i = 0; i < str.length(); i++) {
    if(str.startsWith(".xyz", i)) countFalse++;
    if(str.startsWith("xyz", i)) countTrue++;
  }
  
  return !(countTrue == countFalse);
}
```

## bobThere
```java
public boolean bobThere(String str) {
  for(int i = 0; i < str.length() - 2; i++) {
    if(str.charAt(i) == 'b' && str.charAt(i+2) == 'b') return true;
  }
  return false;
}
```

## xyBalance
```java
public boolean xyBalance(String str) {
  int balance = 0;
  
  for(char c: str.toCharArray()) {
    if(c == 'x') balance++;
    if(c == 'y') balance = 0;
  }
  
  return balance == 0;
}
```

## mixString
```java
public String mixString(String a, String b) {
  int len = a.length() <= b.length() ? a.length() : b.length();
  int i;
  String result = "";
  
  for(i = 0; i < len; i++) {
    result = result + a.charAt(i) + b.charAt(i);
  }
  
  return result + a.substring(i, a.length()) + b.substring(i, b.length());
}
```

## repeatEnd
```java
public String repeatEnd(String str, int n) {
  String result = "";
  
  for(int i = 0; i < n; i++) {
    result = result + str.substring(str.length()-n, str.length());
  }
  
  return result;
}
```

## repeatFront
```java
public String repeatFront(String str, int n) {
  String result = "";
  
  for(int i = 0; i < n; i++) {
    result = result + str.substring(0, n-i);
  }
  
  return result;
}
```

## repeatSeparator
```java
public String repeatSeparator(String word, String sep, int count) {
  String result = "";
  
  for(int i = count; i > 0; i--) {
    result = i > 1 ? result + word + sep : result + word;
  }
  
  return result;
}
```

## prefixAgain
```java
public boolean prefixAgain(String str, int n) {
  String prefix = str.substring(0, n);
  str = str.substring(n, str.length());
  
  for(int i = 0; i < str.length(); i++) {
    if(str.substring(i).startsWith(prefix)) return true;
  }
  
  return false;
}
```

## xyzMiddle
```java
public boolean xyzMiddle(String str) {
  int len = str.length();
  
  if(len < 3) return false;
  
  if(len % 2 != 0) {
    if(str.substring(len/2 - 1, len/2 + 2).equals("xyz")) return true;
  } else {
    if(str.substring(len/2 - 2, len/2 + 1).equals("xyz") ||
       str.substring(len/2 - 1, len/2 + 2).equals("xyz")) return true; 
  }

  return false;
}
```

## getSandwich
```java
public String getSandwich(String str) {
  int firstBread = str.indexOf("bread");
  int secondBread = -1;
  
  for(int i = str.length(); i > 0; i--) {
    secondBread = str.substring(i).indexOf("bread");
    if(secondBread != -1) {
      secondBread = i;
      break;
    }
  }
  
  return firstBread != secondBread
    ? str.substring(firstBread + 5, secondBread)
    : "";
}
```

## sameStarChar
```java
public boolean sameStarChar(String str) {
  
  for(int i = 1; i < str.length() - 1; i++) {
    if(str.charAt(i) == '*' && str.charAt(i-1) != str.charAt(i+1)) {
      return false;
    }
  }
  
  return true;
}
```

## oneTwo
```java
public String oneTwo(String str) {
  String result = "";
  
  for(int i = 0; i < str.length(); i += 3) {
    if(i + 2 < str.length()) {
      result = result + str.charAt(i+1) + str.charAt(i+2) + str.charAt(i);  
    }
  }
  
  return result;
}
```

## zipZap
```java
public String zipZap(String str) {
  String result = "";
  
  for(int i = 0; i < str.length(); i++) {
    if(!(i != 0 && i != str.length() - 1 &&
        str.charAt(i-1) == 'z' && str.charAt(i+1) == 'p')) {
      result += str.charAt(i);  
    }
  }
  
  return result;
}
```

## starOut
```java
public String starOut(String str) {
  String result = "";
  boolean removePrev = false;
  boolean removeNext = false;
  
  for(int i = 0; i < str.length(); i++) {
    if(str.charAt(i) == '*') {
      if(removePrev) {
        result = result.substring(0, result.length() - 1);
        removePrev = false;
      }
      removeNext = true;
    } else {
      if(removeNext) {
        removeNext = false;
        continue;
      }
      result += str.charAt(i);
      removeNext = false;
      removePrev = true;
    }
  }
  
  return result;
}
```

## plusOut
```java
public String plusOut(String str, String word) {
  String result = "";
  int inc = word.length();
  int i = 0;
  
  while(i < str.length()) {
    if(str.substring(i).startsWith(word)) {
      result += word;
      i += inc;
    } else {
      result += "+";
      i++;
    }
  }
  
  return result;
}
```

## wordEnds
```java
public String wordEnds(String str, String word) {
  String result = "";
  
  for(int i = 0; i < str.length(); i++) {
    if(str.substring(i).startsWith(word)) {
      if(i > 0) result += str.charAt(i-1);
      if(i < str.length() - word.length()) result += str.charAt(i+word.length());
    };
  }
  
  return result;
}
```