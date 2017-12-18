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
public int last2(String str) {
  int len = str.length();
  int count = 0;
  
  if(len > 2) {
    String subString = str.substring(len - 2, len);
  
    for(int i = 0; i < len - 2; i++) {
      if(str.substring(i, i + 2).equals(subString)) count++;
    }
  }
  
  return count;
}
```

## arrayCount9
```java
public int arrayCount9(int[] nums) {
  int count = 0;
  for(int n: nums) {
    if(n == 9) count++;
  }
  return count;
}
```

## arrayFront9
```java
public boolean arrayFront9(int[] nums) {
  int count = 0;
  int len = nums.length >= 4 ? 4 : nums.length;

  for(int i = 0; i < len; i++) {
    if(nums[i] == 9) count++;
  }
    
  return count > 0;
}
```

## array123
```java
public boolean array123(int[] nums) {
  for(int i = 0; i < nums.length - 2; i++) {
    if(nums[i] == 1 && nums[i + 1] == 2 && nums[i + 2] == 3) return true;
  }
  return false;
}
```

## stringMatch
```java
public int stringMatch(String a, String b) {
  int count = 0;
  int len = Math.min(a.length(), b.length()) - 1;
  
  for(int i = 0; i < len; i++) {
    if(a.substring(i, i + 2).equals(b.substring(i, i + 2))) count++;
  }
  return count;
}
```

## stringX
```java
public String stringX(String str) {
  String result = "";
  
  for(int i = 0; i < str.length(); i++) {
    if(str.charAt(i) == 'x' && !(i == 0 || i == str.length() -1)) continue;
    result = result + str.charAt(i);
  }
  return result;
}
```

## altPairs
```java
public String altPairs(String str) {
  String result = "";
  
  for(int i = 0; i < str.length(); i++) {
    if(i % 4 == 0 || i % 4 == 1) result+= str.charAt(i);
  }
  return result;
}
```

## stringYak 
```java
public String stringYak(String str) {
  String result = "";
  
  for(int i = 0; i < str.length(); i++) {
      result += str.charAt(i);
      if(result.length() >= 3 &&
        result.charAt(result.length() - 1) == 'k' &&
        result.charAt(result.length() - 3) == 'y') {
          result = result.substring(0, result.length() - 3);
        }
  }
  return result;
}
```

## array667
```java
public int array667(int[] nums) {
  int count = 0;
  
  for(int i = 0; i < nums.length - 1; i++) {
    if(nums[i] == 6 && (nums[i+1] == 6 || nums[i+1] == 7)) count++;
  }
  return count;
}
```

## noTriples
```java
public boolean noTriples(int[] nums) {
  int count = 0;
  int marker = 0;
  
  for(int n: nums) {
    if(marker == n) {
      count++;
    } else {
      count = 1;
      marker = n;
    }
    if(count == 3) return false;
  }
  return true;
}
```

## has271
```java
public boolean has271(int[] nums) {
  for(int i = 0; i < nums.length - 2; i++) {
    if(nums[i] == (nums[i+1] - 5) &&
      Math.abs(nums[i] - 1 - nums[i+2]) <= 2)
        return true;
  }
  return false;
}
```