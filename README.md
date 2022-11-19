# Style Guide for Wordle Final Project

### Constants
Constants should be defined at the top of the class. There should be no arbitrary values such as ints and strings in the code.

```java
// Good example
public class Grid {
  private final static int numRows = 6;
  private final static String wordleString = "Wordle";
  
  public int getRows() { return numRows; }
}
```

```java
// Bad example
public class Grid {
  
  public int getRows() { return 6; }
}
```

### Bracketing
Try to use inline bracketing as much as possible. If a function is a one liner (getter/setter), keep the function on one line like in the example above
Use brackets for one line if statements/for loops

```java
public static void main(String[] args) { // Method opening bracked is on same line
  int x = 5;
  if (x > 4) { // brackets are used for a one line if statement
    x = 2;
  } else {
    x = 10;
  }
}
```
