## 1. Write a program to find length of a string.
### Input
Input string: I love programming. I love Codeforwin.
### Output
Length of string: 38
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        System.out.print("Length of the string: "+str.length());
    }
}
```
## 2. Write a program to copy one string to another string.
### Input
Input string: I love Codeforwin!0
### Output
Original string: I love Codeforwin!
Copied string: I love Codeforwin
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        String s = str;
        System.out.println("Original string: "+str);
        System.out.println("Copied string: "+s);
    }
}
```
## 3. Write a C program to concatenate two strings.
### Input
Input string1: I love
Input string2: Codeforwin
### Output
Concatenated string: I love Codeforwin
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        String s = in.nextLine();

        System.out.println("Concatenated string: "+str.concat(" ").concat(s)); // str + " " + s
    }
}
```
## 4. Write a C program to compare two strings.
### Input
Input string1: Learn at Codeforwin.
Input string2: Learn at Codeforwin.
### Output
Both strings are lexographically equal.
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        String s = in.nextLine();

        if(str.equals(s)){ //str.compareTo(s) == 0
            System.out.println("Both strings are lexographically equal.");
        }else{
            System.out.println("Both strings are not lexographically equal.");
        }
    }
}
```
## 5. Write a C program to convert lowercase string to uppercase.
### Input
Input string: I love Codeforwin.
### Output
I LOVE CODEFORWIN.
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        System.out.println(str.toUpperCase());
    }
}
```
## 6. Write a C program to convert uppercase string to lowercase.
### Input
Input string: I love CODEFORWIN.
### Output
Lowercase string: i love codeforwin.
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        System.out.println(str.toLowerCase());
    }
}
```
## 7. Write a C program to toggle case of each character of a string.
### Input
Input string: Learn at Codeforwin.
### Output
Toggled case string: lEARN aT cODEFORWIN.
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        StringBuilder s = new StringBuilder();
        for(int i=0;i<str.length();i++){
            if(i == 0 || str.charAt(i-1) == ' '){
                s.append(Character.toLowerCase(str.charAt(i)));
            }else{
                s.append(Character.toUpperCase(str.charAt(i)));
            }
        }
        System.out.println(s.toString());
    }
}
```
## 8. Write a C program to find total number of alphabets, digits or special characterin a string.
### Input
Input string: I love Codeforwin.
### Output
Alphabets = 15
Digits = 0
Special characters = 3
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        int digit =0,alpha=0,//special = 0;
        for(char c : str.toCharArray()){
            if(Character.isAlphabetic(c)){
                alpha++;
            }else if(Character.isDigit(c)){
                digit++;
            }
            //else{
            //    special++;
            //}
        }

        System.out.println("Alphabets: "+ alpha + ", Digits: " +digit + ", Special characters: " + (str.length() - digits + alpha);
    }
}
```
## 9.Write a C program to count total number of vowels and consonants in a string.
### Input
Input string: I love Codeforwin.
### Output
Total Vowels = 7
Total Consonants = 8
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        int vowel = 0,consonant=0;
        for(char c : str.toLowerCase().toCharArray()){
            if(c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u'){
                vowel++;

            }else{
                if(Character.isAlphabetic(c)){
                    consonant++;
                }
            }
        }

        System.out.println("Vowels: " + vowel + ", Consonants: " + consonant);
    }
}
```
## 10. Write a C program to count total number of words in a string.
### Input
Input string: I love Codeforwin.
### Output
Total number of words: 4
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        int count = 1;
        for(int i=1;i<str.length();i++){
            if(str.charAt(i-1) == ' '){
                count++;
            }
        }
        System.out.println("Total number of words: " + count); //str.split("\\s+").length
    }
}
```
## 11. Write a C program to find reverse of a string.
### Input
Input String: Hello
### Output
olleH
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        for(int i=0;i<str.length();i++){
            System.out.print(str.charAt(str.length()-1 - i));
        }
    }
}
```
## 12. Write a C program to check whether a string is palindrome or not.
### Input
Input string: madam
### Output
Palindrome string
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        boolean isPal =false;
        for(int i=0;i<str.length();i++){
            if(str.charAt(i) != str.charAt(str.length() - 1 - i)){
                System.out.println("Not Palindrome string");
                isPal = true;
                break;
            }
        }
        if(!isPal){
            System.out.println("Palindrome string");
        }

    }
}
```
## 13. Write a C program to reverse order of words in a given string.
### Input
Input string : I love learning programming at Codeforwin
### Output
Reversed order of words:
Codeforwin at programming learning love I
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        String[] arr = str.split(" ");
        for(int i=0;i<arr.length;i++){
           System.out.print(arr[arr.length - 1 -i] + " ");
        }

    }
}
```
## 14. Write a C program to find first occurrence of a character in a given string.
### Input
Input string: I love Codeforwin.
Input character to search: o
### Output
'o' is found at index 3
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        char ch = in.next().charAt(0);
        System.out.println(str.indexOf(ch));
    }
}
```
## 15. Write a C program to find last occurrence of a character in a given string.
### Input
Input string: I love Codeforwin.
Input character to search: o
### Output
Last index of 'o' is 12.
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        char ch = in.next().charAt(0);
        System.out.println(str.lastIndexOf(ch));
    }
}
```
## 16. Write a C program to search all occurrences of a character in given string.
### Input
Input string: I love programming. I love Codeforwin.
Input character to search: o
### Output
'o' found at index: 3, 9, 23, 28, 32
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        List<Integer> arr = new ArrayList<>();
        String str = in.nextLine();
        char ch = in.next().charAt(0);
        for (int i=0;i<str.length();i++){
            if(str.charAt(i) == ch){
                arr.add(i);
            }
        }
        System.out.println(Arrays.toString(arr.toArray()));
    }
}
```
## 17. Write a C program to count occurrences of a character in given string.
### Input
Input string: I love programming. I love Codeforwin.
Input character to search: o
### Output
Total occurrences of 'o': 5
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        char ch = in.next().charAt(0);
        int cnt=0;
        for(char c: str.toCharArray()){
            if(c == ch){
                cnt++;
            }
        }
        System.out.println(cnt);
    }
}
```
## 18. Write a C program to find highest frequency character in a string.
### Input
Input string: I love Codeforwin.
### Output
Maximum occurring character: 'o'
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        int[] arr = new int[26];
        for(char c : str.toLowerCase().toCharArray()){
            if(Character.isAlphabetic(c)){
                arr[c -'a']++;
            }
        }

        int max = Integer.MIN_VALUE;
        int idx = 0;
        for(int i=0;i<26;i++){
            if(arr[i] > max){
                max = arr[i];
                idx = i;
            }
        }

        System.out.println((char) (idx + 'a'));
    }
}
```
## 19. Write a C program to find lowest frequency character in a string.
### Input
Input string: I love learning programming at Codeforwin.
### Output
Minimum occurring character is '.' = 1
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        Map<Character,Integer> mp = new HashMap<>();

        for(char c : str.toCharArray()){
            mp.put(c,mp.getOrDefault(c,0)+1);
        }

        int min = Integer.MAX_VALUE;
        Map.Entry<Character,Integer> entry = null;
        for(Map.Entry<Character,Integer> e : mp.entrySet()){
            if(e.getValue() < min){
                min = e.getValue();
                entry = e;
            }
        }
        if(entry != null){
            System.out.println(entry.getKey() + " " + entry.getValue());
        }
    }
}
```
## 20. Write a C program to count frequency of each character in a string.
### Input
Input string: Codeforwin
### Output
Frequency of all characters in the given string:
'c' = 1
'd' = 1
'e' = 1
'f' = 1
'i' = 1
'n' = 1
'o' = 2
'r' = 1
'w' = 1
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        Map<Character,Integer> mp = new HashMap<>();

        for(char c : str.toCharArray()){
            mp.put(c,mp.getOrDefault(c,0)+1);
        }

        Map.Entry<Character,Integer> entry = null;
        for(Map.Entry<Character,Integer> e : mp.entrySet()){
            System.out.println(e.getKey() + " = " + e.getValue());
        }

    }
}
```
## 21. Write a C program to remove first occurrence of a character from string.
### Input
Input string: I Love programming. I Love Codeforwin. I Love India.
Input character to remove: 'I'
### Output
Love Programming. I Love Codeforwin. I Love India
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        char ch = in.next().charAt(0);
        StringBuilder s = new StringBuilder();
        boolean isreplaced =false;
        for(char c : str.toCharArray()){
            if(c == ch && !isreplaced ){
                isreplaced = true;
            }else {
                s.append(c);
            }
        }
        System.out.println(s.toString());  //System.out.println(str.replaceFirst(String.valueOf(ch), ""));
    }
}
```
## 22. Write a C program to remove last occurrence of a character from string.
### Input
Input string : I love programming. I love Codeforwin.
Input character to remove : 'I'
### Output
String after removing last 'I' : I love programming. love Codeforwin.
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        char ch = in.next().charAt(0);
        StringBuilder s = new StringBuilder();
        boolean isreplaced =false;
        for(int i=str.length()-1;i>=0;i--){
            if(str.charAt(i) == ch && !isreplaced ){
                isreplaced = true;
            }else {
                s.append(str.charAt(i));
            }
        }
        System.out.println(s.reverse().toString());
    }
}
```
## 23. Write a C program to remove all occurrences of a character from string.
### Input
Input string : I Love Programming. I Love Codeforwin.
Input character to remove : 'I'
### Output
String after removing all 'I' : Love Programming. Love Codeforwin.
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        char ch = in.next().charAt(0);
        StringBuilder s = new StringBuilder();
        for(char c : str.toCharArray()){
            if(c != ch){
                s.append(c);
            }
        }

        System.out.println(s.toString());
    }
}
```
## 24. Write a C program to remove all repeated characters from a given string.
### Input
Input string: Programming in C.
### Output
String after removing duplicate characters: Progamin C.
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        StringBuilder s = new StringBuilder().append(str.charAt(0));
        for(int i=1;i<str.length();i++){
            if(str.charAt(i-1) != str.charAt(i)){
                s.append(str.charAt(i));
            }
        }
        System.out.println(s);

    }
}
```
## 25. Write a C program to replace first occurrence of a character with another in a string.
### Input
Input string: I love programming.
Input character to replace: .
Input character to replace with: !
### Output
String after replacing '.' with '!': I love programming!
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        char ch = in.next().charAt(0);
        char r = in.next().charAt(0);

        StringBuilder s = new StringBuilder();
        boolean isreplaced = false;
        for(char c : str.toCharArray()){
            if(c == ch && !isreplaced){
                s.append(r);
                isreplaced = true;
            }else s.append(c);
        }
        System.out.println(s);

    }
}
```
## 26. Write a C program to replace last occurrence of a character with another in a string.
###Input
Input string: Do you love programming.
Input character to replace: .
Input character to replace with: ?
### Output
String after replacing last '.' with '?' : Do you love programming?
```
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        char ch = in.next().charAt(0);
        char r = in.next().charAt(0);

        StringBuilder s = new StringBuilder();
        boolean isreplaced = false;
        for(int i=str.length() -1 ;i >=0;i--){
            if(str.charAt(i) == ch && !isreplaced){
                s.append(r);
                isreplaced = true;
            }else s.append(str.charAt(i));
        }
        System.out.println(s.reverse());

    }
}
```
## 27. Write a C program to replace all occurrences of a character with another in astring.
### Input
Input string: I_love_learning_at_Codeforwin.
Input character to replace: _
Input character to replace with: -
### Output
String after replacing '_' with '-': I-love-learning-at-Codeforwin
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        String str = in.nextLine();
        char ch = in.next().charAt(0);
        char r = in.next().charAt(0);

        StringBuilder s = new StringBuilder();
       for(char c : str.toCharArray()){
           if(c == ch){
               s.append(r);
           }else s.append(c);
       }
        System.out.println(s);

    }
}
```





