# ShortenerWithSixStrategies
This mini programm can make unique short strings from any strings/URLs.  
Example:  
```java
public class Solution {
    public static void main(String[] args) {
        Shortener shortener = new Shortener(new HashBiMapStorageStrategy());
        //originUrl
        String originUrl = "https://github.com/bigsam40/";
        System.out.println(originUrl);

        //convert URL to id
        Long stringId = shortener.getId(originUrl);
        System.out.println(stringId);

        //convert id back to URL
        String stringFromId = shortener.getString(stringId);
        System.out.println(stringFromId);
    }
}
```  
The main logic of the program is located in the Shortener class.   
An instance of this class requires passing a strategy from the strategy package when created.  
This program was written with the goal of learning the Strategy design pattern.  
Additionally, during the creation of the program, libraries such as Guava, Apache Commons Collections, and Junit were applied to cover the functionality of the strategies with automated tests and evaluate their effectiveness.
