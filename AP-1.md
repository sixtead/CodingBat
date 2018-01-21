# AP-1

## scoresIncreasing
```java
public boolean scoresIncreasing(int[] scores) {
  for(int i = 1; i < scores.length; i++) {
    if(scores[i] < scores[i - 1]) {
      return false;
    }
  }
  return true;
}
```

## scores100
```java
public boolean scores100(int[] scores) {
  for(int i = 1; i < scores.length; i++) {
    if(scores[i] == scores[i-1] && scores[i] == 100) {
      return true;
    }
  }
  return false;
}
```

## scoresClump
```java

```