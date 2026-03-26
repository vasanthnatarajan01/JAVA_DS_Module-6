# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE:  26-02-2026
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Start.

2. Declare an array to store sensor readings.

3. Define a recursive function findMin(arr, n):

   If n == 1, return arr[0].

   Otherwise, return the minimum of:

     arr[n-1]

     findMin(arr, n-1)

4. Call the recursive function from main().

5. Display the minimum value.

6. Stop.

## Program:
``` JAVA
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: KARTHIK SARAVANAN B
RegisterNumber:  212224230118
*/

import java.util.Scanner;

public class RecursiveMinimum {

    // Recursive method to find minimum value
    static int findMin(int arr[], int n) {
        if (n == 1) {
            return arr[0];
        }
        
        return Math.min(arr[n - 1], findMin(arr, n - 1));
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of sensor readings: ");
        int n = sc.nextInt();

        int arr[] = new int[n];

        System.out.println("Enter sensor readings:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int minimum = findMin(arr, n);

        System.out.println("Minimum value (Lowest Heartbeat): " + minimum);

        sc.close();
    }
}
```

## Output:

<img width="449" height="281" alt="Screenshot 2026-02-19 221001" src="https://github.com/user-attachments/assets/905f7b60-5134-434f-97b3-85be6c9b21f0" />


## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
