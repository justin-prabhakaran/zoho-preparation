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
        int sum = 0;
        for(int i=0;i<n;i++){
            sum += arr[i];
        }
        System.out.println(sum);
    }
}
```
OR
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

        System.out.println(Arrays.stream(arr).sum());
    }
}
```
## 3. Write a program to input elements in an array from user, find maximum and minimum element in array.
### Sample Input:
Input array elements: 10, 50, 12, 16, 2
### Sample Output:
Maximum = 50\
Minimum = 2
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int max = Integer.MIN_VALUE;
        for(int i=0;i<n;i++){
            int k = in.nextInt();
            max = Math.max(max,k);
        }
        System.out.println(max);
    }
}
```
OR
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int[] arr = new int[n];
        for(int i=0;i<n;i++) {
            arr[i] = in.nextInt();
        }
        OptionalInt max = Arrays.stream(arr).max();
        if(max.isPresent()){
            System.out.println(max.getAsInt());
        }
    }
}
```
OR 
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        TreeSet<Integer> arr = new TreeSet<>();
        for(int i=0;i<n;i++){
            arr.add(in.nextInt());
        }
        System.out.println(arr.last());

    }
}
```
## 4. Write a program to find second largest element in an array.
### Sample Input:
Input array elements: -7 2 3 8 6 6 75 38 3 2
### Sample Output:
Second largest = 38
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int[] arr = new int[n];
        for(int i=0;i<n;i++) {
            arr[i] = in.nextInt();
        }
        int max1 = Integer.MIN_VALUE;
        int max2 = Integer.MIN_VALUE;
        
        for(int i : arr){
            if(i > max1){
                max2 = max1;
                max1 = i;
            } else if (i > max2) {
                max2 = i;    
            }
        }
        System.out.println(max2);
    }
}
```
OR
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        TreeSet<Integer> arr = new TreeSet<>();
        for(int i=0;i<n;i++){
            int k = in.nextInt();
            arr.add(k);
            if(arr.size() > 2){
                arr.pollFirst();
            }
        }
        System.out.println(arr.first());

    }
}
```
## 5. Write a program to input elements in array from user and count even and odd elements in array.
### Sample Input:
Input array: 1 2 3 4 5 6 7 8 9
### Sample Output:
Total even elements: 4\
Total odd elements: 5
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int ev=0,od = 0;
        for(int i=0;i<n;i++){
            int k = in.nextInt();
            if(k%2 == 0){
                ev++;
            }else od++;
        }
        System.out.println("Even: " + ev + " Odd: "+ od);
    }
}
```
## 6. Write a program to input elements in array and count negative elements in array.
### Sample Input:
Input array elements: 10, -2, 5, -20, 1, 50, 60, -50, -12, -9
### Sample Output:
Total number of negative elements: 5
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int cnt=0;
        for(int i=0;i<n;i++){
            int k = in.nextInt();
            if(k < 0){
                cnt++;
            }
        }
        System.out.println(cnt);
    }
}
```
## 7. Write a C program to input elements in array and copy all elements of first arrayinto second array.
### Sample Input:
Input array1 elements: 10 1 95 30 45 12 60 89 40 -4
### Sample Output:
Array1: 10 1 95 30 45 12 60 89 40 -4\
Array2: 10 1 95 30 45 12 60 89 40 -4
```
    I dont know y do we need that shit! <Time waste>
```
## 8. Write a program to insert element in array at specified position.
### Sample Input:
Input array elements: 10, 20, 30, 40, 50\
Input element to insert: 25\
Input position where to insert: 3
### Sample Output:
Elements of array are: 10, 20, 25, 30, 40, 50
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int[] arr = new int[n+1];
        for(int i=0;i<n;i++){
           arr[i] = in.nextInt();
        }
        int el = in.nextInt();
        int k = in.nextInt();

        for(int i=n;i>k;i--){
            arr[i] = arr[i-1];
        }
        arr[k] = el;
        System.out.println(Arrays.toString(arr));

    }
}
```
## 9. Write a program to delete element from array at specified position.
### Sample Input:
Input array elements: 10 20 30 40 50\
Input position to delete: 2
### Sample Output:
Array elements: 10, 30, 40, 50
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
        int k = in.nextInt();

        for(int i=k;i<n-1;i++){
            arr[i] = arr[i+1];
        }
        System.out.println(Arrays.toString(Arrays.copyOfRange(arr, 0, n - 1)));

    }
}
```
## 10. Write a program to input elements in array and find frequency of each element in array.
### Sample Input:
Input array elements: 5, 10, 2, 5, 50, 5, 10, 1, 2, 2
### Sample Output:
Frequency of 5 = 3\
Frequency of 10 = 2\
Frequency of 2 = 3\
Frequency of 50 = 1\
Frequency of 1 = 1
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
        int max = Arrays.stream(arr).max().getAsInt(); //lets assume always present
        int[] hash = new int[max+1];
        for(int i=0;i<n;i++){
            hash[arr[i]]++;
        }

       for(int i=0;i< hash.length;i++){
           if(hash[i] != 0){
               System.out.println(i + "=" + hash[i]);
           }
       }

    }
}
```
## 11. Write a program to input elements in array and print all unique elements in array.
### Sample Input:
Input array elements: 1, 2, 3, 5, 1, 5, 20, 2, 12, 10
### Sample Output:
All unique elements in the array are: 3, 20, 12, 10
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
        Arrays.sort(arr);
        for(int i=1;i<n-1;i++){
            if(arr[i-1] == arr[i]){
                for(int j=i;j<n-1;j++){
                    arr[j] = arr[j+1];
                }
                n--;
            }
        }
        for(int i=0;i<n;i++){
            System.out.print(arr[i] + " ");
        }

    }
}
```
## 12. Write a program to input elements in array from user and count duplicate elements in array.
### Sample Input:
Input array elements: 1, 10, 20, 1, 25, 1, 10, 30, 25, 1
### Sample Output:
Total number of duplicate elements = 5
```
    i cant understand this qs!!
```

## 13. Write a program to delete duplicate elements from array. How to remove duplicate elements from array in C programming.
### Sample Input:
Input array elements: 10, 20, 10, 1, 100, 10, 2, 1, 5, 10
### Sample Output:
After removing all duplicate elements\
Elements of array are: 10, 20, 1, 100, 2, 5\

refer [this](#11-write-a-program-to-input-elements-in-array-and-print-all-unique-elements-in-array)

## 14. Write a program to input elements in two array and merge two array to third array.
### Input
Input first array elements: 1, 4, 6, 9, 15\
Input second array elements: 2, 5, 8, 10
### Output
Merged array in ascending order = 1, 2, 4, 5, 6, 8, 9, 10, 15
```java
import java.util.*;
import java.io.*;
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n1 = in.nextInt();
        int[] arr1 = new int[n1];
        for(int i=0;i<n1;i++){
            arr1[i] = in.nextInt();
        }
        int n2 = in.nextInt();
        int[] arr2 = new int[n2];
        for(int i=0;i<n2;i++){
            arr2[i] = in.nextInt();
        }
        int[] arr = new int[n1+ n2];
        int i=0,j=0,k=0;
        while(i < n1 && j < n2){
            if(arr1[i] < arr2[j]){
                arr[k] = arr1[i];
                i++;
            }else {
                arr[k] = arr2[j];
                j++;
            }
            k++;
        }
        while(i < n1){
            arr[k] = arr1[i];
            i++;
            k++;
        }
        while(j < n2){
            arr[k] = arr2[j];
            j++;
            k++;
        }

        System.out.println(Arrays.toString(arr));
    }
}
```
## 15. Write a program to input elements in array and find reverse of array.
### Sample Input:
Input array elements: 10, 5, 16, 35, 500
### Sample Output:
Array elements after reverse: 500, 35, 16, 5, 10
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
           System.out.print(arr[n-1-i] + " ");
       }
    }
}
```
## 16. Write a program to input elements in array and put even and odd elements in separate array.
### Sample Input:
Input size of the array: 10\
Input elements in array: 0 1 2 3 4 5 6 7 8 9
### Sample Output:
Output even elements in array: 0 2 4 6 8\
Output odd elements in array: 1 3 5 7 9
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

        int[] even = new int[n];
        int[] odd = new int[n];
        int ev=0,od=0,i=0;
        while(i < n){
            if(arr[i] % 2 == 0){
                even[ev++] = arr[i++];
            }else {
                odd[od++] = arr[i++];
            }
        }

        for(int j=0;j<ev;j++){
            System.out.print(even[j] + " ");
        }
        System.out.println();
        for(int j=0;j<od;j++){
            System.out.print(odd[j] + " ");
        }
    }
}
```
## 17. Write a program to input elements in array and search whether an element exists in array or not.
### Sample Input:
Input size of array: 10\
Input elements in array: 10, 12, 20, 25, 13, 10, 9, 40, 60, 5
### Sample Output:
Element to search is: 25\
Element found at index 3
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
        int el = in.nextInt();
        for(int i=0;i<n;i++){
            if(arr[i] == el){
                System.out.println(i);
            }
        }
    }
}
```
## 18. Write a program to input elements in array and sort array elements in ascending or descending order.
## Sample Input:
Input size of array: 10\
Input array elements: 20, 2, 10, 6, 52, 31, 0, 45, 79, 40
## Sample Output:
Array sorted in ascending order: 0, 2, 6, 10, 20, 31, 40, 45, 52, 79
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
            for(int j=i;j>0;j--){
                if(arr[j-1] > arr[j]){
                    int temp = arr[j-1];
                    arr[j-1] = arr[j];
                    arr[j] =temp;
                }else{
                    break;
                }
            }
        }
        System.out.println(Arrays.toString(arr));
    }
}
```
OR 
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
        System.out.println(Arrays.toString(Arrays.stream(arr).sorted().toArray()));
    }
}
```
## 19. Write a program to input elements in an array from user and sort all even and odd elements of the given array separately without using any other array.
### Sample Input:
Input size of array: 10\
Input elements of array: 0 5 1 2 3 4 6 12 10 9
### Sample Output:
Output in sorted order: 0 2 4 6 10 12 1 3 5 9
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

        int i=0,j=n-1;
        while(i < j){
            while(i < n && arr[i] % 2 == 0 ) i++;
            while(j >= 0 && arr[j] % 2 != 0) j--;

            if(i < j){
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }

        }

        Arrays.sort(arr,0,i);  //use above sort algorithm to avoid build-in func
        Arrays.sort(arr,i,n);
        System.out.println(Arrays.toString(arr));
    }
}
```
## 20. Write a program to left rotate an array by n position
### Sample Input:
Input 10 elements in array: 1 2 3 4 5 6 7 8 9 10\
Input number of times to rotate: 3
### Sample Output:
Array after left rotation 3 times: 4 5 6 7 8 9 10 1 2 3
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
        int k = in.nextInt();
        rotate(arr,0,k-1);
        rotate(arr,k,n-1);
        rotate(arr,0,n-1);

        System.out.println(Arrays.toString(arr));
    }
    private static void rotate(int[] arr, int i, int j){
        while (i < j){
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
            i++;
            j--;
        }

    }
}
```
## 21. Write a C program to right rotate an array by n position.
### Sample Input:
Input 10 elements in array: 1 2 3 4 5 6 7 8 9 10\
Input number of times to rotate: 3
### Sample Output:
Array after right rotation: 8 9 10 1 2 3 4 5 6 7
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
        int k = in.nextInt();
        rotate(arr,0,n-1);
        rotate(arr,0,k-1);
        rotate(arr,k,n-1);

        System.out.println(Arrays.toString(arr));
    }
    private static void rotate(int[] arr, int i, int j){
        while (i < j){
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
            i++;
            j--;
        }

    }
}
```




