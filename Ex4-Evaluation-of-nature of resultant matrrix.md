# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE: 19/3/26
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
