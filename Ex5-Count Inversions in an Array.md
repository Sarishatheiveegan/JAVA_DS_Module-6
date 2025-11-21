## Ex5 Count Inversions in an Array
## DATE: 20/08/2025
## AIM:
To write a Java program to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1.Read the size of the array n and input all elements into the array arr.

2.Initialize an inversion counter count = 0.

3.Use two nested loops:

Outer loop: index i from 0 to n−1

Inner loop: index j from i+1 to n−1

4.For every pair (i, j), check:

If arr[i] > arr[j], then increment the inversion counter.

5.After all comparisons, output the total count of inversions.

## Program:

Program to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
```
import java.util.*;

public class CountInversions {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();         
        int[] arr = new int[n];
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();

        System.out.println(countInversions(arr, n));
    }

    static int countInversions(int[] arr, int n) {
        int count = 0;
        for (int i = 0; i < n - 1; i++) {
            for (int j = i + 1; j < n; j++) {
                if (arr[i] > arr[j])
                    count++;
            }
        }
        return count;
    }
}
```
## Output:
<img width="756" height="380" alt="image" src="https://github.com/user-attachments/assets/2aed73ed-93a1-45ec-b054-dba653f8f382" />

## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
