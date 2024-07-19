## 1. Given a list of integers, shift all the zeros to the end of the list while maintaining the relative order of the non-zero elements. Modify the list in place.
### Sample Input and Output
Input: [0, 1, 0, 3, 12]\
Output: [1, 3, 12, 0, 0]
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n= in.nextInt();
        int[] arr = new int[n];
        for(int i=0;i<n;i++){
            arr[i] = in.nextInt();
        }

        for(int i=0;i<n;i++){
            if(arr[i] == 0){
                for(int j=i;j<n-1;j++){
                    int temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                }
            }
        }
        System.out.println(Arrays.toString(arr));
    }
}
```
### Output:
```
/usr/lib/jvm/default/bin/java -javaagent:/var/lib/snapd/snap/intellij-idea-community/515/lib/idea_rt.jar=36441:/var/lib/snapd/snap/intellij-idea-community/515/bin -Dfile.encoding=UTF-8 -classpath /home/crazyshit/IdeaProjects/sample/out/production/sample Main
5
1 0 2 0 3
[1, 2, 3, 0, 0]

Process finished with exit code 0
```
## 2. Given an integer n, generate an n x n matrix filled with elements from 1 to n2n^2n2 in a spiral order. The matrix should be filled in a clockwise direction starting from the top-left corner.
### Input
An integer n (1 ≤ n ≤ 20).
### Output
A 2D list (list of lists) representing the n x n matrix filled with integers in spiral order.
```java
import java.lang.reflect.Array;
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n= in.nextInt();
        int[][] arr = new int[n][n];
        for(int i=0;i<n;i++){
            for(int j=0;j<n;j++){
                arr[i][j] = in.nextInt();

            }
        }

        int top=0,down = n-1;
        int left=0,right = n-1;

        int[] ans = new int[n*n];
        int k=0;
        while (top <= down && left <= right){

            for(int i=left;i<=right;i++){
                ans[k++] = arr[top][i];
            }
            top++;

            for(int i=top;i<=down;i++){
                ans[k++] = arr[i][right];
            }
            right--;

            if(top <= down){
                for(int i=right;i>=left;i--){
                    ans[k++] = arr[down][i];
                }
                down--;
            }

            if(left <= right){
                for(int i=down;i>=top;i--){
                    ans[k++] = arr[i][left];
                }
                left++;
            }


        }
        System.out.println(Arrays.toString(ans));
    }
}
```
### Output:
```
/usr/lib/jvm/default/bin/java -javaagent:/var/lib/snapd/snap/intellij-idea-community/515/lib/idea_rt.jar=39345:/var/lib/snapd/snap/intellij-idea-community/515/bin -Dfile.encoding=UTF-8 -classpath /home/crazyshit/IdeaProjects/sample/out/production/sample Main
4
1  2  3  4
5  6  7  8
9 10 11 12
13 14 15 16
[1, 2, 3, 4, 8, 12, 16, 15, 14, 13, 9, 5, 6, 7, 11, 10]

Process finished with exit code 0
```
## 3. Problem Statement: Rotate Matrix 90 Degrees Clockwise
### Description
Given an n x n matrix, rotate the matrix by 90 degrees clockwise in-place.
### Input
An n x n 2D list (list of lists) representing the matrix, where 1≤n≤1001\leq n \leq 1001≤n≤100.
### Output
The same 2D list after it has been rotated 90 degrees clockwise.
### Example
Example 1:\
Input:\
matrix = [\
 [1, 2, 3],\
 [4, 5, 6],\
 [7, 8, 9] ]\
Output:\
[\
 [7, 4, 1],\
 [8, 5, 2],\
 [9, 6, 3]\
]
```java

import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n= in.nextInt();
        int[][] arr = new int[n][n];
        for(int i=0;i<n;i++){
           for(int j=0;j<n;j++){
               arr[i][j] = in.nextInt();
           }
        }
        for(int i=0;i<n;i++){
            for(int j=i;j<n;j++){
                int temp = arr[i][j] ;
                arr[i][j] = arr[j][i];
                arr[j][i] = temp;
            }
        }
        for(int i=0;i<n;i++){
            for(int j=0;j<n/2;j++){
                int temp = arr[i][j];
                arr[i][j] = arr[i][n-1-j];
                arr[i][n-1-j] = temp;
            }
        }

        System.out.println(Arrays.deepToString(arr));
    }
}
```
### Output:
```
/usr/lib/jvm/default/bin/java -javaagent:/var/lib/snapd/snap/intellij-idea-community/515/lib/idea_rt.jar=35623:/var/lib/snapd/snap/intellij-idea-community/515/bin -Dfile.encoding=UTF-8 -classpath /home/crazyshit/IdeaProjects/sample/out/production/sample Main
4
1  2  3  4
5  6  7  8
9 10 11 12
13 14 15 16
[[13, 9, 5, 1], [14, 10, 6, 2], [15, 11, 7, 3], [16, 12, 8, 4]]

Process finished with exit code 0
```


## 4. Given a string, perform basic string compression using the counts of repeated characters.
### Input and Output
Example 1:\
Input: "aabcccccaaa"\
Output: "a2b1c5a3"
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String str = in.next();

        StringBuilder s = new StringBuilder();
        for(int i=0;i<str.length();i++){
            int cnt=1;
            s.append(str.charAt(i));
            int j=i;
            while(j+1 < str.length() && str.charAt(j) == str.charAt(j+1)){
                cnt++;
                j++;
            }
            i = j;
            s.append(cnt);
        }

        System.out.println(s);
    }
}
```
