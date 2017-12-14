# Warmup - 1

## sleepIn
```java
public boolean sleepIn(boolean weekday, boolean vacation) {
  return !weekday || vacation;
}
```

## monkeyTrouble
```java
public boolean monkeyTrouble(boolean aSmile, boolean bSmile) {
  return aSmile == bSmile;
}
```

## sumDouble
```java
public int sumDouble(int a, int b) {
  if(a == b) return a * 4;
  return a + b;
}
```

## diff21
```java
public int diff21(int n) {
  if(n > 21) return (n - 21) * 2;
  return 21 - n;
}
```

## parrotTrouble
```java
public boolean parrotTrouble(boolean talking, int hour) {
  if(hour < 7 || hour > 20) return talking;
  return false;
}
```

## makes10
```java
public boolean makes10(int a, int b) {
  if(a == 10 || b == 10 || a + b == 10) return true;
  return false;
}
```

## nearHundred
```java
public boolean nearHundred(int n) {
  if(n >= 90 && n <= 110) return true;
  if(n >= 190 && n <= 210) return true;
  return false;
}
```

## posNeg
```java
public boolean posNeg(int a, int b, boolean negative) {
  // return (!negative && ((a<0 && b>0) || (a>0 && b<0))) || (negative && (a<0 && b <0));
  // converted with wolfram
  return negative ^ a > 0 ^ b > 0 ^ (negative && a > 0 && b > 0);
}
```

## notString
```java
public String notString(String str) {
  if(str.split(" ")[0].equals("not")) return str;
  return "not " + str;
}
```

## missingChar
```java
public String missingChar(String str, int n) {
  return str.substring(0, n) + str.substring(n + 1, str.length());
}
```

## frontBack
```java
public String frontBack(String str) {
  if(str.length() <= 1) return str;
  return str.charAt(str.length() - 1) + 
    str.substring(1, str.length() - 1) + 
    str.charAt(0);
}
```

## front3
```java
public String front3(String str) {
  if(str.length() > 3) str = str.substring(0, 3);
  return str + str + str;
}
```

## backAround
```java
public String backAround(String str) {
  return str.charAt(str.length() - 1) + str + str.charAt(str.length() - 1);
}
```

## or35
```java
public boolean or35(int n) {
  return n % 3 == 0 || n % 5 == 0;
}
```

## front22
```java
public String front22(String str) {
  if(str.length() > 2) return str.substring(0, 2) + str + str.substring(0, 2);
  return str + str + str;
}
```

## startHi
```java
public boolean startHi(String str) {
  return str.startsWith("hi");
}
```

## icyHot
```java
public boolean icyHot(int temp1, int temp2) {
  return (temp1>100 && temp2<0) || (temp1<0 && temp2>100);
}
```

## in1020
```java
public boolean in1020(int a, int b) {
  return (a >= 10 && a <= 20) || (b >= 10 && b <= 20);
}
```

## hasTeen
```java
public boolean hasTeen(int a, int b, int c) {
  return (a >= 13 && a <= 19) || (b >= 13 && b <= 19) || (c >= 13 && c <= 19);
}
```

## loneTeen
```java
public boolean loneTeen(int a, int b) {
  return (a >= 13 && a <= 19) ^ (b >= 13 && b <= 19);
}
```

## delDel
```java
public String delDel(String str) {
  if(str.startsWith("del", 1)) return str.charAt(0) + str.substring(4);
  return str;
}
```

## mixStart
```java
public boolean mixStart(String str) {
  return str.startsWith("ix", 1);
}
```

## startOz
```java
public String startOz(String str) {
  if(str.startsWith("o")) return str.startsWith("z", 1) ? "oz" : "o";
  if(str.startsWith("z", 1)) return "z";
  return "";
}
```

## intMax
```java
public int intMax(int a, int b, int c) {
  int max = a;
  if(b > max) max = b;
  if(c > max) max = c;
  return max;
}
```

## close10
```java
public int close10(int a, int b) {
  if(Math.abs(a - 10) > Math.abs(b - 10)) return b;
  if(Math.abs(a - 10) < Math.abs(b - 10)) return a;
  return 0;
}
```

## in3050
```java
public boolean in3050(int a, int b) {
  return ((a >= 30 && a <= 40) && (b >= 30 && b <= 40)) ||
    ((a >= 40 && a <= 50) && (b >= 40 && b <= 50));
}
```
## max1020
```java
public int max1020(int a, int b) {
  int max = 0;
  if(a >= 10 && a <= 20 && a > max) max = a;
  if(b >= 10 && b <= 20 && b > max) max = b;
  return max;
}
```

## stringE
```java
public boolean stringE(String str) {
  int count = 0;
  for(char ch: str.toCharArray()) {
    if(ch == 'e') count++;
  }
  return count > 0 && count < 4;
}
```

## lastDigit
```java
public boolean lastDigit(int a, int b) {
  return a % 10 == b % 10;
}
```

## endUp
```java
public String endUp(String str) {
  int len = str.length();
  if(len >= 3) {
    str = str.substring(0, len - 3) + str.substring(len - 3, len).toUpperCase();
  } else {
    str = str.toUpperCase();
  }
  return str;
}
```

## everyNth
```java
public String everyNth(String str, int n) {
  String res = "" + str.charAt(0);
  for(int i = 1; i < str.length(); i++) {
    if(i % n == 0) res = res + str.charAt(i);
  }
  return res;
}
```

#