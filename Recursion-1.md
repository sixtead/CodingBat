# Recursion-1

## factorial
```java
public int factorial(int n) {
  return (n == 1) ? 1 :  n * factorial(n - 1);
}
```

## bunnyEars
```java
public int bunnyEars(int bunnies) {
  return bunnies == 0 ? 0 : 2 + bunnyEars(bunnies - 1);
}
```

## fibonacci
```java
public int fibonacci(int n) {
  if(n == 0) {
    return 0;
  } else if(n == 1) {
    return 1;
  } else {
    return fibonacci(n - 2) + fibonacci(n - 1);
  }
}
```

## bunnyEars2
```java
public int bunnyEars2(int bunnies) {
  if(bunnies == 0) {
    return 0;
  } else {
    return (bunnies % 2 == 0)
      ? 3 + bunnyEars2(bunnies - 1)
      : 2 + bunnyEars2(bunnies - 1);
  }
}
```

## triangle
```java
public int triangle(int rows) {
  return rows == 0 ? 0 : rows + triangle(rows - 1);
}
```

## sumDigits
```java
public int sumDigits(int n) {
  return n == 0 ? 0 : n % 10 + sumDigits(n / 10);
}
```

## count7
```java
public int count7(int n) {
  if(n == 0) {
    return 0;
  } else {
    return n % 10 == 7 ? 1 + count7(n / 10) : count7(n / 10);
  }
}
```

## count8
```java
public int count8(int n) {
  if(n == 0) {
    return 0;
  } else {
    if(n % 10 == 8) {
      return (n / 10) % 10 == 8 ? 2 + count8(n / 10) : 1 + count8(n / 10);
    }
    return count8(n / 10);
  }
}
```

## powerN
```java
public int powerN(int base, int n) {
  return n == 0 ? 1 : base * powerN(base, n - 1);
}
```

## countX
```java
public int countX(String str) {
  int len = str.length();
  
  if(len == 0) {
    return 0;
  } else {
    return str.charAt(len - 1) == 'x'
      ? 1 + countX(str.substring(0, len - 1))
      : countX(str.substring(0, len - 1));
  }
}
```

## countHi
```java
public int countHi(String str) {
  int len = str.length();
  if(len < 2) {
    return 0;
  } else {
    return str.substring(len - 2, len).equals("hi")
      ? 1 + countHi(str.substring(0, len - 2))
      : countHi(str.substring(0, len - 1));
  }
}
```

## changeXY
```java
public String changeXY(String str) {
  if(str.length() == 0) {
    return str;
  } else {
    char ch = str.charAt(0) == 'x' ? 'y' : str.charAt(0);
    return ch + changeXY(str.substring(1));
  }
}
```

## changePi
```java
public String changePi(String str) {
  int len = str.length();
  if(len < 2) {
    return str;
  } else {
    int step;
    String pi;
    if(str.substring(0, 2).equals("pi")) {
      step = 2;
      pi = "3.14";
    } else {
      step = 1;
      pi = str.substring(0, 1);
    }
    return pi + changePi(str.substring(step));
  }
}
```

## noX
```java
public String noX(String str) {
  if(str.length() == 0) {
    return str;
  } else {
    return str.charAt(0) == 'x'
      ? noX(str.substring(1))
      : str.charAt(0) + noX(str.substring(1));
  }
}
```

## array6
```java
public boolean array6(int[] nums, int index) {
  if(index == nums.length) {
    return false;
  } else if(nums[index] == 6) {
    return true;
  } else {
    return array6(nums, index + 1);
  }
}
```

## array11
```java
public int array11(int[] nums, int index) {
  if(index == nums.length) {
    return 0;
  } else if(nums[index] == 11) {
    return 1 + array11(nums, index + 1);
  } else {
    return array11(nums, index + 1);
  }
}
```

## array220
```java
public boolean array220(int[] nums, int index) {
  if(index == nums.length) {
    return false;
  } else {
    if(index < nums.length - 1 && nums[index] * 10 == nums[index+1]) {
      return true;
    }
    return array220(nums, index+ 1);
  }
}
```

## allStar
```java
public String allStar(String str) {
  if(str.length() < 2) {
    return str;
  } else {
    return str.charAt(0) + "*" + allStar(str.substring(1));
  }
}
```

## pairStar
```java
public String pairStar(String str) {
  if(str.length() < 2) {
    return str;
  } else {
    String ch = str.charAt(0) == str.charAt(1)
      ? str.charAt(0) + "*"
      : "" + str.charAt(0);

    return ch + pairStar(str.substring(1));
  }
}
```

## endX
```java
public String endX(String str) {
  if(str.length() == 0) {
    return str;
  } else {
    return str.charAt(0) == 'x'
      ? endX(str.substring(1)) + 'x'
      : str.charAt(0) + endX(str.substring(1));
  }
}
```

## countPairs
```java

```