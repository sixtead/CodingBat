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
public boolean scoresClump(int[] scores) {
  for(int i = 2; i < scores.length; i++) {
    if(scores[i-2] <= scores[i-1] && scores[i-1] <= scores[i]
        && scores[i] - scores[i-2] <= 2) {
      return true;
    }
  }
  return false;
}
```

## scoresAverage
```java
public int scoresAverage(int[] scores) {
  return Math.max(average(scores, 0, scores.length / 2),
                  average(scores, scores.length / 2, scores.length));
}

int average(int[] scores, int start, int end) {
  int sum = 0;
  for(int i = start; i < end; i++) {
    sum += scores[i];
  }
  
  return sum / (end - start);
}
```

## wordsCount
```java
public int wordsCount(String[] words, int len) {
  int count = 0;
  
  for(String word: words) {
    if(word.length() == len) {
      count++;
    }
  }
  
  return count;
}
```

## wordsFront
```java
public String[] wordsFront(String[] words, int n) {
  return Arrays.copyOf(words, n);
}
```

## wordsWithoutList
```java
public List wordsWithoutList(String[] words, int len) {
  List<String> filteredWords = new ArrayList<>();
  
  for(String word: words) {
    if(word.length() != len) {
      filteredWords.add(word);
    }
  }
  
  return filteredWords;
}
```

## hasOne
```java
public boolean hasOne(int n) {
  return String.valueOf(n).contains("1");
}
```

## dividesSelf
```java
public boolean dividesSelf(int n) {
  int rightmostDigit = 0;
  int num = n;
  
  while(num > 10) {
    rightmostDigit = num % 10;
    if(rightmostDigit == 0 || n % rightmostDigit != 0) {
      return false;
    }
    num = num / 10;
  }
  
  return n % num == 0;
}
```

## copyEvens
```java
public int[] copyEvens(int[] nums, int count) {
  int index = 0;
  int[] evenNums = new int[count];
  
  for(int n: nums) {
    if(n % 2 == 0 && index < count) {
      evenNums[index++] = n;
    }
  }
  
  return evenNums;
}
```

## copyEndy
```java
public int[] copyEndy(int[] nums, int count) {
  int index = 0;
  int[] endyNums = new int[count];
  
  for(int n: nums) {
    if(isEndy(n) && index < count) {
      endyNums[index++] = n;
    }
  }
  
  return endyNums;
}

boolean isEndy(int n) {
  return (n >= 0 && n <= 10) || (n >= 90 && n <= 100);
}
```

## matchUp
```java
public int matchUp(String[] a, String[] b) {
  int count = 0;
  
  for(int i = 0; i < a.length; i++) {
    if(!a[i].isEmpty() && !b[i].isEmpty() && a[i].charAt(0) == b[i].charAt(0)) {
      count++;
    }
  }
  
  return count;
}
```

## scoreUp
```java
public int scoreUp(String[] key, String[] answers) {
  int score = 0;
  
  for(int i = 0; i < answers.length; i++) {
    if(answers[i].equals(key[i])) {
      score += 4;
    } else if(answers[i].equals("?")) {
      score += 0;
    } else {
      score--;
    }
  }
  
  return score;
}
```

## wordsWithout
```java
public String[] wordsWithout(String[] words, String target) {
  int length = 0;
  String[] filteredWords = new String[0];
  
  for(String word: words) {
    if(!word.equals(target)) {
      filteredWords = Arrays.copyOf(filteredWords, length + 1);
      filteredWords[length++] = word;
    }
  }
  
  return filteredWords;
}
```

## scoresSpecial
```java
public int scoresSpecial(int[] a, int[] b) {
  return largestSpecialScore(a) + largestSpecialScore(b);
}

int largestSpecialScore(int[] scores) {
  int maxScore = 0;
  
  for(int score: scores) {
    if(score % 10 == 0) {
      maxScore = Math.max(maxScore, score);
    }
  }
  
  return maxScore;
}
```

## sumHeights
```java

```