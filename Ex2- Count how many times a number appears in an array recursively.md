# Ex2 Count how many times a number appears in an array recursively.
## DATE: 26-02-2026
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm

1. Start

2. Read the number of elements (n)

3. Read the array elements

4. Read the number to be counted (key)

5. If n equals 0, return 0

6. If the last element of the array equals key, add 1

7. Call the recursive function with n minus 1

8. Add the result of recursive call to the count

9. Display the total count

10. Stop

## Program:
```
/* 
Program Count how many times a number appears in an array recursively.

Developed by: karthik saravanan b
Register Number: 212224230118
*/

import java.util.Scanner;

public class RecursiveCount {

    // Recursive method to count occurrences
    static int countOccurrences(int arr[], int n, int key) {
        if (n == 0) {
            return 0;
        }

        if (arr[n - 1] == key) {
            return 1 + countOccurrences(arr, n - 1, key);
        } else {
            return countOccurrences(arr, n - 1, key);
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int arr[] = new int[n];

        System.out.println("Enter elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.print("Enter number to count: ");
        int key = sc.nextInt();

        int result = countOccurrences(arr, n, key);

        System.out.println("Number of times " + key + " appears: " + result);

        sc.close();
    }
}


```

## Output:

<img width="393" height="290" alt="Screenshot 2026-02-19 221844" src="https://github.com/user-attachments/assets/3c9b0686-89d6-4805-93c8-47c2b74d32ba" />

## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
