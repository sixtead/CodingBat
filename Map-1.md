# Map-1

## mapBully
```java
public Map<String, String> mapBully(Map<String, String> map) {
  if(map.containsKey("a")) {
    map.put("b", map.get("a"));
    map.put("a", "");
  }
  
  return map;
}
```

## mapShare
```java
public Map<String, String> mapShare(Map<String, String> map) {
  if(map.containsKey("a")) {
    map.put("b", map.get("a"));
  }
  
  map.remove("c");
  
  return map;
}
```

## mapAB
```java
public Map<String, String> mapAB(Map<String, String> map) {
  if(map.containsKey("a") && map.containsKey("b")) {
    map.put("ab", map.get("a") + map.get("b"));
  }
  
  return map;
}
```

## topping1
```java
public Map<String, String> topping1(Map<String, String> map) {
  if(map.containsKey("ice cream")) map.put("ice cream", "cherry");
  map.put("bread", "butter");
  
  return map;
}
```

## topping2
```java
public Map<String, String> topping2(Map<String, String> map) {
  if(map.containsKey("ice cream")) map.put("yogurt", map.get("ice cream"));
  if(map.containsKey("spinach")) map.put("spinach", "nuts");
  
  return map;
}
```

## topping3
```java
public Map<String, String> topping3(Map<String, String> map) {
  if(map.containsKey("potato")) map.put("fries", map.get("potato"));
  if(map.containsKey("salad")) map.put("spinach", map.get("salad"));
  
  return map;
}
```

## mapAB2
```java
public Map<String, String> mapAB2(Map<String, String> map) {
  if(map.containsKey("a") && map.containsKey("b")
      && map.get("a").equals(map.get("b"))) {
    map.remove("a");
    map.remove("b");
  }
  
  return map;
}
```

## mapAB3
```java
public Map<String, String> mapAB3(Map<String, String> map) {
  if(map.containsKey("a") && !map.containsKey("b")) map.put("b", map.get("a"));
  if(map.containsKey("b") && !map.containsKey("a")) map.put("a", map.get("b"));
  
  return map;
}
```

## mapAB4
```java
public Map<String, String> mapAB4(Map<String, String> map) {
  if(map.containsKey("a") && map.containsKey("b")) {
    if(map.get("a").length() == map.get("b").length()) {
      map.put("a", "");
      map.put("b", "");
    } else {
      String value = map.get("a").length() > map.get("b").length()
          ? map.get("a")
          : map.get("b");
      map.put("c", value);
    }
  }
  
  return map;
}
```