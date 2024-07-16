# 1 D Array Exercises
## 1. Write a program to input elements in array and print all negative elements.
### Sample Input:
10\
-1
-10
100
5
61
-2
-23
8
-90
51
### Sample Output:
-1, -10, -2, -23, -90
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int[] arr = new int[n];

        for(int i=0;i<n;i++){
            arr[i] = in.nextInt();
        }

        for(int i=0;i<n;i++){
            if(arr[i] < 0){
                System.out.print(arr[i] + " ");
            }
        }
    }
}
```
## 2. Write a program to read elements in an array and find the sum of array elements.
### Sample Input:
Input elements: 10, 20, 30, 40, 50
### Sample Output:
Sum of all elements = 150
```
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int[] arr = new int[n];

        for(int i=0;i<n;i++){
            arr[i] = in.nextInt();
        }
        int sum = 0;
        for(int i=0;i<n;i++){
            sum += arr[i];
        }
        System.out.println(sum);
    }
}
```
