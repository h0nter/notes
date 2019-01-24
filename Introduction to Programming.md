# Introduction to Programming
## My example answers
---
### Question 2:

```java
public class Token{
  private char root;
  private Token[] multi;
  
  public Token(char root)
  {
      this.root = root;
  }
  
  public Token(String word)
  {
      multi = new Token[word.length()];
      for (int i = 0; i < word.length(); i++)
      {
          multi[i] = new Token(word.getCharAt(i));
      }
  }
  
  public char randomToken()
  {
      if (multi.equals(null))
      {
          return new Token('z');
      }else{
          return new Token(int(Math.random() * (multi.length - 1)));
      }
  }
  
  public int nMultis(char c)
  {
      if (multi.equals(null))
      {
          return 0;
      }else{
          int sum = 0;
          for (int i = 0; i < multi.length; i++)
          {
              if (multi[i].getRoot().equals(c))
              {
                  sum++;
              }
          }
          return sum;
      }
  }
  
  //I added it myself to avoid making 'root' variable public
  public char getRoot()
  {
      return root;
  }
}
```
