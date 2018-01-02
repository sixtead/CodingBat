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