# Map-2

## word0
```java
public Map<String, Integer> word0(String[] strings) {
  Map<String, Integer> map = new HashMap<>();
  for(String str : strings) {
    if(!map.containsKey(str)) map.put(str, 0);
  }
  
  return map;
}
```

## wordLen
```java
public Map<String, Integer> wordLen(String[] strings) {
  Map<String, Integer> map = new HashMap<>();
  
  for(String key : strings) {
    if(!map.containsKey(key)) map.put(key, key.length());
  }
  
  return map;
}
```

## pairs
```java
public Map<String, String> pairs(String[] strings) {
  Map<String, String> map = new HashMap<>();
  
  for(String str : strings) {
    map.put(str.substring(0, 1), str.substring(str.length() - 1));
  }
  
  return map;
}
```

## wordCount
```java
public Map<String, Integer> wordCount(String[] strings) {
  Map<String, Integer> map = new HashMap<>();
  
  for(String key : strings) {
    int value = (map.containsKey(key))
        ? map.get(key) + 1
        : 1;
        
    map.put(key, value);
  }
  
  return map;
}
```

## firstChar
```java
public Map<String, String> firstChar(String[] strings) {
  Map<String, String> map = new HashMap<>();
  
  for(String str : strings) {
    String key = str.substring(0, 1);
    String value = (map.containsKey(key))
        ? map.get(key) + str
        : str;
        
    map.put(key, value);
  }
  
  return map;
}
```

## wordAppend
```java
public String wordAppend(String[] strings) {
  Map<String, Integer> map = new HashMap<>();
  String result = "";
  
  for(String str : strings) {
    int value = (map.containsKey(str))
        ? map.get(str) + 1
        : 1;
        
    map.put(str, value);
    
    result = (value % 2 == 0) ? result + str : result;
  }
  return result;
}
```

## wordMultiple
```java
public Map<String, Boolean> wordMultiple(String[] strings) {
  Map<String, Boolean> map = new HashMap<>();
  Boolean value;
  String prev = "";
  int count = 1;
  
    Arrays.sort(strings);
    
  for(String key : strings) {
    if(key.equals(prev)) {
      count++;
    } else {
      prev = key;
      count = 1;
    }
    
    value = (count > 1) ? true : false;
    map.put(key, value);
  }
  
  return map;
}
```

## allSwap
```java
public String[] allSwap(String[] strings) {
  Map<String, Integer> map = new HashMap<>();
  
  for(int i = 0; i < strings.length; i++) {
    String key = strings[i].substring(0, 1);
    if(!map.containsKey(key)) {
      map.put(key, i);
    } else {
      String tmp = strings[i];
      strings[i] = strings[map.get(key)];
      strings[map.get(key)] = tmp;
      map.remove(key);
    }
  }

  return strings;
}
```

## firstSwap
```java
public String[] firstSwap(String[] strings) {
  Map<String, Integer> map = new HashMap<>();
  
  for(int i = 0; i < strings.length; i++) {
    String key = strings[i].substring(0, 1);
    if(!map.containsKey(key)) {
      map.put(key, i);
    } else if(map.containsKey(key) && map.get(key) != -1) {
      String tmp = strings[i];
      strings[i] = strings[map.get(key)];
      strings[map.get(key)] = tmp;
      map.put(key, -1);
    }
  }

  return strings;
}
```