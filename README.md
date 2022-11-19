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

### Static methods
All private/helper methods should be static and all public methods should be non-static. Avoid using this.<variable> as much as possible.

```java
public class Game {
  
  private final static int numRows = 6;
  
  // public non-static method
  public List<String> evaluateGuesses() {
    List<String> guesses = new List<String>();
    for (int i = 0; i < numRows; i++) {
        guesses.add(evaluateGuess(i);
    }
    return guesses;
  }
  
  // private static method
  private static String evaluateGuess(int i) {
    ...
  }
  
}
```

### Spacing
Keep spacing between mathematical operations, for loops, declarations, and comparisons

```java
// Good example
int x = 5;
int x += 1;
if (y < x) {}
public int get() { return x; }
```

```java
// Bad example
int x=5;
int x+=1;
if (y<x) {}
public int get() {return x;}
```

### Spacing (cont.)
Keep one line of whitespace between every method in a function.
Avoid having whitespace inside functions as much as possible.
Keep one line of whitespace between the top/bottom functions and the class brackets.
         
```java        
 public class Player {
         
   private final static int numGuesses = 6;
         
   public Player() {}
   
   // function comment
   public int getGuesses() {}
         
   // function comment      
   public int makeMove() {
      ...
   }
       
   // function comment      
   private static void isPlaying() {}

}
``` 
   
### Class initializers/setters
Since we are trying to avoid the use of this.<varaible>, class initializers should be set up like this
  
```java
public class Dog {
  
  private static String name;
  private static String breed;
  
  public Dog(String newName, String newBreed) {
    name = newName;
    breed = newBreed;
  }
  
  public void setName(String newName) { name = newName; }
 
}
```
