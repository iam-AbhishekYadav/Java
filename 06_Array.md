# # Arrays in Java

- Arrays allow us to store multiple values of the same type in a single variable.
- They are useful for storing and managing collections of data.

<img src="https://github.com/user-attachments/assets/93e7c52e-f7bf-43f5-b3cb-4b6040acfbe8" width="500" height="300">

## Key features of Arrays:

- Contiguous Memory Allocation (for Primitives)
- Zero-based Indexing
- Fixed Length
- Can Store Primitives & Objects

# # Creating an Array

### Syntax :-

**1. To Construct an Array**  

(i) 1st Way ---> **`dataType arrayName[] = new dataType[size];`**  

(ii) 2nd Way ---> **`dataType[] arrayName = new dataType[size];`**  

<img src="https://github.com/user-attachments/assets/b6cc3f0b-28a0-461f-b11f-f5900f482733" width="500" height="300">

<br>
<br>

**2. To Access an Element**   

**`dataType arrayName[] = {---List of Initial Values---};`**  

### Example --->

``` java
public class Abhi{
    public static void main(String args[]){

        int[] abhi = new int[50];                           // By default Stored 0

        int numbers[] = {1,2,3,4,5};                        // Size = 5

        String[] fruits = {"Apple", "Mango", "Orange"};      // Size = 3
    }
}
```

# # Input / Output / Update on Array

``` java
import java.util.*;
public class Abhi{
    public static void main(String args[]){

        Scanner sc = new Scanner(System.in);

        int marks[] = new int[100];

        marks[0] = sc.nextInt();                                            // Input : 90
        marks[1] = sc.nextInt();                                            // Input : 75
        marks[2] = sc.nextInt();                                            // Input : 80

        System.out.println("Physics :" +marks[0]);                          // Output : Physics : 90
        System.out.println("Chemistry :" +marks[1]);                        // Output : Chemistry : 75
        System.out.println("Maths :" +marks[2]);                            // Output : Maths : 80

        marks[2] = 89;                                                      // Update Maths marks by 89
        System.out.println("Maths :" +marks[2]);                            // Output : Maths : 89                         

        marks[1] = marks[1] + 2;                                            // Update Chemistry marks by +2
        System.out.println("Chemistry :" +marks[1]);                        // Output : Chemistry : 77


        int percentage = (marks[0] + marks[1] + marks[2]) / 3;             // Calculating % 
        System.out.println("Percentage = " + percentage + "%");            // Percentage : 85 (According to updated marks)
    }
}
```

## Array as Function Arguments

- When we pass an array to a method as an argument, **`actually the address of the array in the memory is passed (reference)`**.
- Therefore, any changes to this array in the method will affect the array.

### Example -->

``` java
public class Abhi{
    public static void update(int marks[] , int nonChangeable){

        nonChangeable = 10;

        for (int i = 0; i < marks.length; i++){
            marks[i] = marks[i] + 1;
        }
    }

    public static void main(String args[]){

        int marks[] = {97, 98, 99};
        int nonChangeable = 5;

        update(marks , nonChangeable);

        System.out.println(nonChangeable);                         // Output : 5 (Call by Value)

        for (int i = 0; i < marks.length; i++) {
            System.out.print(marks[i] + " ");                     // Output : 98 99 100 (Call by Referance)
        }
        System.out.println();
    }
}
```

# # Linear Search 

- It also known as sequential search.
- It is a simple method for finding a target element within a list or array.
-  It operates by iterating through each element of the list one by one, comparing it with the target element until a match is found or the end of the list is reached.

### Example --->

``` java
public class Abhi{
    public static int linearSearch(int[] arr, int target) {
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == target) {
                return i;                                         // Return the index if the target is found
            }
        }
        return -1;                                                // Return -1 if the target is not found
    }

    public static void main(String args[]){

        int[] numbers = {5, 2, 9, 1, 5, 6};
        int target = 9;
        
        int index = linearSearch(numbers, target);                  // Output : Element found at index : 2

        if (index != -1) {
            System.out.println("Element found at index : " + index);              
        } else {
            System.out.println("Element not found in the array");
        }
    }
}
```

# # Largest Number 

- In Java utility package (import java.util.*;)
  - **`- ∞`** --> Integer. MIX_VALUE
  - **`+ ∞`** --> Integer. MAX_VALUE



### Ques --> Find the largest number in a given array {1 , 2 , 6 , 3 , 5}

We compare all numbers by **- ∞** , then we get largest number.

``` java
import java.util.*;
public class Abhi{
    public static int getLargest(int number[]){

        int largest = Integer.MIN_VALUE;

        for (int i = 0; i < number.length; i++) {
            if (largest < number[i]){
                largest = number[i];
            }
        }
        return largest;   
    }

    public static void main(String args[]){

        int number[] = {1 , 2 , 6 , 3 , 5};

        System.out.println("Largest number of Array is :"+ getLargest(number));         // Output : Largest number of Array is : 6

    }
}
```

# # Binary Search

- It is an efficient algorithm for finding a target value within a sorted array.
  - Sorted Array --> Elements are arranged in a specific order (Ascending or Descending)  

### How it Works : 

**`Step-1`** &nbsp; Check the value in the center of the array.  
**`Step-2`** &nbsp; If the target value is lower, search the left half of the array. If the target value is higher, search the right half.  
**`Step-3`** &nbsp; Continue step 1 and 2 for the new reduced part of the array until the target value is found or until the search area is empty.  
**`Step-4`** &nbsp; If the value is found, return the target value index. If the target value is not found, return -1.  

<img src="https://github.com/user-attachments/assets/da10f574-33c8-4776-8100-0185befb6ad2" width="500" height="500">

### Pseudo Code :

**`1`** &nbsp; Start  
**`2`** &nbsp; Take input array and Target  
**`3`** &nbsp; Initialise start = 0 and end = (array size -1)  
**`4`** &nbsp; Intialise mid variable  
**`5`** &nbsp; Mid = (start+end)/2  
**`6`** &nbsp; if array[mid] == target then return mid  
**`7`** &nbsp; if array[mid] < target then start = mid+1  
**`8`** &nbsp; if array[mid] > target then end = mid-1  
**`9`** &nbsp; if start<=end then goto step 5  
**`10`** &nbsp; Return -1 as target not found  
**`11`** &nbsp; Exit  

### Code --->

``` java
import java.util.*;
public class Abhi{
    public static int binarySearch(int number[], int key){

        int start = 0 , end = number.length-1;

        while (start <= end) {

            int mid = (start + end) / 2;

            if (number[mid] == key) {
                return mid;
            }

            if (number[mid] < key) {
                start = mid + 1;
            }

            else{
                end = mid - 1;
            }
            
        }
        return -1 ;
        
    }

    public static void main(String args[]){

        int number[] = {1 , 2, 3, 4, 5, 6, 7, 8, 9, 10} ;
        int key = 7;

        System.out.println("Index for Key is :" + binarySearch(number, key));            // Output : Index for Key is : 6
    }
}
```

# # Time & Space Complexity

**`Time Complexity`** ---> The amount of time required by the algorithm to execute to completion.

> [!IMPORTANT] 
> **Time Complexity ∝ log<sub>2</sub>n**  
>  **Time Complexity = Olog<sub>2</sub>n**

**`Space Complexity`** ---> The amount of memory space needed the algorithm in its life cycle.

> [!IMPORTANT]
> **Space Complexity = O(1)**















