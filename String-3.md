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

## 