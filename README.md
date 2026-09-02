# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Start the program.
2. Read the number of elements (e.g., number of heartbeat readings).
3. Store all readings in an array.
4. Call a recursive function findMin(arr, index) If index == arr.length - 1, return arr[index] Else return min(arr[index], findMin(arr, index + 1))  
5. Print the minimum value returned by the recursive function. 

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: JAISREE N
RegisterNumber: 212224060104
*/
import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) {
        if (i == n - 1) {
            return arr[i];
        }
        int minRest = getMin(arr, i + 1, n);
        return Math.min(arr[i], minRest);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}
```

## Output:

<img width="814" height="316" alt="image" src="https://github.com/user-attachments/assets/f11fd834-c0ab-4269-9c02-de0d13391ca6" />


## Result:
Thus the JAVA program to find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully



# Ex2 Count how many times a number appears in an array recursively.

## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1. Start the program.
2. Read the size of the array and input all elements into the array. 
3. Read the target number whose frequency you want to count.
4. Call the recursive function countOccurrences(arr, index, target) If index == arr.length, return 0 If arr[index] == target, return 1 + countOccurrences(arr, index + 1, target) Else return countOccurrences(arr, index + 1, target) 
5. Display the returned count as the total number of occurrences.  

## Program:
```
/*
Program Count how many times a number appears in an array recursively.
Developed by: JAISREE N
RegisterNumber: 212224060104
*/
import java.util.Scanner;

public class CountOccurrences {
    public static int countOccurrences(int[] arr, int n, int target) {
        if (n == 0) {
            return 0;
        }
        if (arr[n - 1] == target) {
            return 1 + countOccurrences(arr, n - 1, target);
        } else {
            return countOccurrences(arr, n - 1, target);
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int size = scanner.nextInt();

        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }

        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }

        // Input: Target number to count
        int target = scanner.nextInt();

        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");

        scanner.close();
    }
}
```

## Output:
<img width="1043" height="628" alt="image" src="https://github.com/user-attachments/assets/72a90608-15d2-4616-9254-4269e5017b63" />


## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.

# EX3 Write a program to count the number of digits in an integer.

## AIM:
To write a java program to count the number of digits in an integer.

## Algorithm
2. Read an integer input num from the user.
3. If num is equal to 0, then the number has 1 digit.
4. Convert num to its absolute value to handle negative numbers.
5. Initialize a counter variable count = 0.
6. Repeat the following steps while num > 0:
Divide num by 10 (integer division).
Increment count by 1.
7. After the loop ends, count will contain the number of digits.
8.  Display the value of count.
9. End the program.  

## Program:
```
/*
Program to to count the number of digits in an integer
Developed by: JAISREE N
RegisterNumber: 212224060104
*/
import java.util.Scanner;

public class CountDigits {

    public static int countDigits(int num) {
        int count = 0;
        if (num == 0) return 1; 
        num = Math.abs(num);   
        while (num > 0) {
            count++;
            num /= 10;
        }
        return count;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        int digits = countDigits(num);
        System.out.println("Number of digits: " + digits);
    }
}
```

## Output:

<img width="785" height="301" alt="image" src="https://github.com/user-attachments/assets/262f4a30-0311-4cd3-82de-b44843630170" />



## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.

# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?

## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm

1. Start the program.
2. Read the number of rows rows and columns cols.
3. Create three 2D arrays.
4. Input elements for Matrix A.
5. Input elements for Matrix B.
6. Perform matrix addition
7. After each row is printed, move to the next line.
8. End the program.

## Program:
```
/*
Program to ind the nature of resultant matrrix.
Developed by: JAISREE N
RegisterNumber: 212224060104
*/
import java.util.Scanner;

public class MatrixAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int rows, cols;

       
        rows = sc.nextInt();
        cols = sc.nextInt();

        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];
        int[][] sum = new int[rows][cols];

        
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                A[i][j] = sc.nextInt();

        
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                B[i][j] = sc.nextInt();

        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                sum[i][j] = A[i][j] + B[i][j];

        
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++)
                System.out.print(sum[i][j] + " ");
            System.out.println();
        }
        sc.close();
    }
}
```

## Output:

<img width="575" height="744" alt="image" src="https://github.com/user-attachments/assets/b31df123-eb14-4170-9367-96c2f4418264" />


## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.

# Ex5 Count Inversions in an Array

## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Start the program.
2. Declare an array arr[] and a variable count = 0 to store the number of inversions.
3. Read the array elements from the user.
4. For each pair of elements (arr[i], arr[j]), check if arr[i] > arr[j] and i < j.
5. If the above condition is true, increment the inversion count.
6. Continue until all pairs are checked.
7. Display the total number of inversions found in the array and stop the program.

## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: JAISREE N
RegisterNumber: 212224060104
*/
import java.util.Scanner;

public class CountInversions {
    public static int mergeSortAndCount(int[] arr, int left, int right) {
        int count = 0;
        if (left < right) {
            int mid = (left + right) / 2;
            count += mergeSortAndCount(arr, left, mid);
            count += mergeSortAndCount(arr, mid + 1, right);
            count += mergeAndCount(arr, left, mid, right);
        }
        return count;
    }

    private static int mergeAndCount(int[] arr, int left, int mid, int right) {
        int[] leftArr = new int[mid - left + 1];
        int[] rightArr = new int[right - mid];

        for (int i = 0; i < leftArr.length; i++) leftArr[i] = arr[left + i];
        for (int i = 0; i < rightArr.length; i++) rightArr[i] = arr[mid + 1 + i];

        int i = 0, j = 0, k = left, swaps = 0;

        while (i < leftArr.length && j < rightArr.length) {
            if (leftArr[i] <= rightArr[j]) {
                arr[k++] = leftArr[i++];
            } else {
                arr[k++] = rightArr[j++];
                swaps += (leftArr.length - i); 
                
            }
       
        }

        while (i < leftArr.length) arr[k++] = leftArr[i++];
        while (j < rightArr.length) arr[k++] = rightArr[j++];

        return swaps;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();
        System.out.println(mergeSortAndCount(arr, 0, n - 1));
    }
}
```

## Output:

<img width="598" height="451" alt="image" src="https://github.com/user-attachments/assets/912cf65e-1735-48bc-a2ec-85e3e48b7caf" />


## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j is implemented successfully.
