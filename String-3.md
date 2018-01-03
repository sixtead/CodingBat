# String-3

## countYZ
```java
public int countYZ(String str) {
  int count = 0;
  String[] words = str.split("[^\\p{Alpha}]");
  
  for(String word: words) {
    if(word.toLowerCase().endsWith("y") ||
       word.toLowerCase().endsWith("z")) {
         count++;
       }
  }
  
  return count;
}
```

## withoutString
```java
public String withoutString(String base, String remove) {
  return base.replace(remove, "")
             .replace(remove.toLowerCase(), "")
             .replace(remove.toUpperCase(), "");
}
```

## equalIsNot
```java
public boolean equalIsNot(String str) {
  int countIs = 0;
  int countNot = 0;
  
  for(int i = 0; i < str.length(); i++) {
    if(str.substring(i).startsWith("is")) countIs++;
    if(str.substring(i).startsWith("not")) countNot++;
  }
  
  return countIs == countNot;
}
```

## gHappy
```java
public boolean gHappy(String str) {
  int g = 0;

  for(int i = 0; i < str.length(); i++) {
    if(str.charAt(i) == 'g') {
      g++;
    } else {
      if(g == 1) return false;
      g = 0;
    }
  }
  
  return g != 1;
}
```

## countTriple
```java
public int countTriple(String str) {
  int count = 0;
  
  for(int i = 0; i < str.length(); i++) {
    String subStr = str.substring(i);
    char c = subStr.charAt(0);
    if(subStr.startsWith("" + c + c + c)) {
      count++;
    }
  }
  
  return count;
}
```

## sumDigits
```java
public int sumDigits(String str) {
  int sum = 0;
  
  for(char c: str.toCharArray()) {
    if(Character.isDigit(c)) {
      sum += Integer.parseInt("" + c);
    }
  }
  
  return sum;
}
```

## sameEnds
```java
public String sameEnds(String string) {
  String result = "";
  
  for(int i = 0; i < string.length() / 2; i++) {
    String beginning = string.substring(0, i+1);
    String end = string.substring(string.length()-i-1, string.length());
    
    if(beginning.equals(end)) result = beginning;
  }
  
  return result;
}
```

## mirrorEnds
```java
public String mirrorEnds(String string) {
  String result = "";
  
  for(int i = 0; i < string.length(); i++) {
    char beginning = string.charAt(i);
    char end = string.charAt(string.length()-i-1);

    if (beginning == end) {
      result = string.substring(0, i+1);
    } else {
      break;
    }
  }
  
  return result;
}
```

## maxBlock
```java
public int maxBlock(String str) {
  int count = 1;
  int max = 0;
  char ch = ' ';
  
  for(int i = 0; i < str.length(); i++) {
    count = (ch == str.charAt(i)) ? count + 1 : 1;
    ch = str.charAt(i);
    max = max < count ? count : max;
  }
  
  return max;
}
```

## sumNumbers
```java
public int sumNumbers(String str) {
  int sum = 0;
  String[] nums = str.split("\\D+");
  
  for(String num: nums) {
    if(!num.isEmpty()) sum += Integer.parseInt(num);
  }
  
  return sum;
}
```

## notReplace
```java
public String notReplace(String str) {
  return str.replaceAll("\\bis\\b", "is not");
}
```