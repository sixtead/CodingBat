## cigarParty
```java
public boolean cigarParty(int cigars, boolean isWeekend) {
  return ((cigars >= 40 && cigars <= 60) || (isWeekend && cigars >= 40));
}
```

## dateFashion
```java
public int dateFashion(int you, int date) {
  if(you <= 2 || date <= 2) return 0;
  if(you >= 8 || date >= 8) return 2;
  return 1;
}
```

## squirrelPlay
```java
public boolean squirrelPlay(int temp, boolean isSummer) {
  return temp >= 60 && (temp <= 90 || (isSummer && temp <= 100));
}
```

## caughtSpeeding
```java
public int caughtSpeeding(int speed, boolean isBirthday) {
  int bonusSpeed = isBirthday ? 5 : 0;
  
  if(speed >= 81 + bonusSpeed) return 2;
  if(speed >= 61 + bonusSpeed) return 1;
  return 0;
}
```

## sortaSum
```java
public int sortaSum(int a, int b) {
  int sum = a + b;
  return sum >= 10 && sum <= 19 ? 20 : sum;
}
```

## alarmClock
```java
public String alarmClock(int day, boolean vacation) {
  if(day != 0 && day != 6) return vacation ? "10:00" : "7:00";
  return vacation ? "off" : "10:00";
}
```

## love6
```java
public boolean love6(int a, int b) {
  return (a == 6 || b == 6 || a + b == 6 || Math.abs(a - b) == 6);
}
```

## in1To10
```java
public boolean in1To10(int n, boolean outsideMode) {
  return (outsideMode && (n <= 1 || n >= 10)) ||
          (!outsideMode && n >= 1 && n <= 10);
}
```

## specialEleven
```java
public boolean specialEleven(int n) {
  return (n % 11 == 0) || (n % 11 == 1);
}
```

## more20
```java
public boolean more20(int n) {
  return n % 20 == 1 || n % 20 == 2;
}
```

## old35
```java
public boolean old35(int n) {
  return n % 3 == 0 ^ n % 5 == 0;
}
```

## less20
```java
public boolean less20(int n) {
  return (n+1) % 20 == 0 || (n+2) % 20 == 0;
}
```

## nearTen
```java
public boolean nearTen(int num) {
  int mod = num % 10;
  return (mod >= 0 && mod <= 2) || (mod >= 8 && mod <= 9);
}
```

## teenSum
```java
public int teenSum(int a, int b) {
  int sum = a + b;
  return (a >= 13 && a <= 19) || (b >= 13 && b <= 19) ? 19 : a + b;
}
```

## answerCell
```java
public boolean answerCell(boolean isMorning, boolean isMom, boolean isAsleep) {
  return !isAsleep && (isMom || !isMorning);
}
```

## teaParty
```java
public int teaParty(int tea, int candy) {
  if(tea < 5 || candy < 5) return 0;
  if(tea / candy >= 2 || candy / tea >= 2) return 2;
  return 1;
}
```

## fizzString
```java
public String fizzString(String str) {
  String fizzBuzz = "";
  if(str.charAt(0) == 'f') fizzBuzz += "Fizz";
  if(str.charAt(str.length() - 1) == 'b') fizzBuzz += "Buzz";
  return fizzBuzz.isEmpty() ? str : fizzBuzz;
}
```

## fizzString2
```java
public String fizzString2(int n) {
  String fizzBuzz = "";
  
  if(n % 3 == 0) fizzBuzz += "Fizz";
  if(n % 5 == 0) fizzBuzz += "Buzz";
  
  return fizzBuzz.isEmpty() ? n + "!" : fizzBuzz + "!";
}
```

## twoAsOne
```java
public boolean twoAsOne(int a, int b, int c) {
  return (a + b == c) || (a + c == b) || (b + c == a);
}
```

## inOrder
```java
public boolean inOrder(int a, int b, int c, boolean bOk) {
  return (c > b) && (bOk || b > a);
}
```

## inOrderEqual
```java
public boolean inOrderEqual(int a, int b, int c, boolean equalOk) {
  return (a < b && b < c) || (equalOk && a <= b && b <= c);
}
```

## lastDigit
```java
public boolean lastDigit(int a, int b, int c) {
  return (a % 10 == b % 10) || (b % 10 == c % 10) || (c % 10 == a % 10);
}
```

## lessBy10
```java
public boolean lessBy10(int a, int b, int c) {
  return (Math.abs(a - b) >= 10) ||
          (Math.abs(b - c) >= 10) ||
          (Math.abs(a - c) >= 10);
}
```

## withoutDoubles
```java

```