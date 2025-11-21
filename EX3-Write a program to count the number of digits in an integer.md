## EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE:06/08/2025
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
Read n and the array elements.
Call getMin(arr, 0, n).
If i is the last index, return arr[i].
Recursively get the minimum of the rest of the array.
Return the smaller value between arr[i] and the recursive result.
## Program:
```
import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) 
    {
        if(i==n-1){
            return arr[i];
        }
        int minRest = getMin(arr, i + 1, n);

    if (arr[i] < minRest) {
        return arr[i];  
    } else {
        return minRest; 
    }
        
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}

```
## Output:
<img width="639" height="256" alt="image" src="https://github.com/user-attachments/assets/8a1ab189-f924-42e3-9baf-6150751edffe" />

## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfull
