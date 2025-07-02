# # Sorting in Java

-  Arranging elements of an array or a collection in a specific order, such as ascending or descending.
-   Tt reduces the complexity of a problem.

<img src="https://github.com/user-attachments/assets/81668ee0-a7b0-44b9-bf50-5f5bf02229a2" width="400" height="250">

## # Types of Sorting

The following two types of sorting algorithms can be broadly classified:

**1. `Comparison-based`** : We compare the elements in a comparison-based sorting algorithm.  
**2. `Non-comparison-based`** : We do not compare the elements in a non-comparison-based sorting algorithm.

<img src="https://github.com/user-attachments/assets/76076a4d-ac3a-4738-9a7c-7210e3cec37a" width="400" height="350">

# # Bubble Sort Algorithm

- Bubble sort works by repeatedly swapping the adjacent elements if they are in the wrong order.
- This algorithm is not suitable for large data sets as its average and worst-case time complexity are quite high.

## How does Bubble Sort Work ?

- Total No. of Passes/Turns/Steps/Certain No. ---> **n-1**
- In every iteration the largest number in part of array to be processed get its correct position.

<img src="https://github.com/user-attachments/assets/8ffd8620-51bd-4e0c-ab58-4091553d2a39" width="500" height="300">  

<img src="https://github.com/user-attachments/assets/8fe42337-c367-403c-abf3-4e118ffd1001" width="500" height="300">  

<img src="https://github.com/user-attachments/assets/a97e389c-7055-45df-a3dc-94b1e690bec3" width="500" height="300">  


## Bubble Sort Code

### Approach

- Outer Loop ---> No. of Iterations/Turns/No. of Steps = **`n-1`**
- Inner Loop ---> Comparing or Swaping
  - **`n-1-i`** ---> Last i elements are alredy at correct sorted position , so no need to check them.
  - **`n-1`** ---> It is also Right but unoptimized.


``` java
public class Abhi {

    public static void bubbleSort(int arr[]){

// n-1 ---> No. of Iterations/Turns/No. of Steps

        for (int i = 0 ; i < arr.length-1; i++) {

// Last i elements are alredy at correct sorted position , so no need to check them

            for (int j = 0; j < arr.length-1-i; j++) {

// Comparison
                if (arr[j] > arr[j+1]) {

// Swaping
                    int temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                }
            }
        }
    }

    public static void main(String[] args) {

        int arr[] = {5, 4, 1, 2, 3, 6, 0};
        bubbleSort(arr);

        for (int i : arr) {
            System.out.print(i + " ");                      Output : 0 1 2 3 4 5 6 
        }
    }
}
```
## Time and Space Complexitiy

- Scape Complexitiy ---> **O(1)**
- Time Complexitiy ---> **O(n<sup>2</sup>)**

## Maximum No. of Swaps in Worst Csae

- In worst case in every comparision/iteration we do swap
- **Swap = `n(n-1)/2`**

## How to optimize the Bubble Sort in the case of nearly sorted arrays ?

- Initialy we compare all elements while array is sorted.
- We optimize the bubble sort if we somehow find out that our current array is already sorted.
- In sorted array we don't swap elements.
- In Best case Time Complexity ---> **O(n)**


``` java
public class Abhi {

    public static void bubbleSort(int arr[]){

        for (int i = 0 ; i < arr.length-1; i++) {

            boolean flag = false;                                // Has any swapping happened

            for (int j = 0; j < arr.length-1-i; j++) {

                if (arr[j] > arr[j+1]) {
                    
                    int temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;

                    flag = true;                                // Some swap happened
                }
            }

            if (!flag) {                                          // Have any swap happened ?
                return;
            }
        }
    }


    public static void main(String[] args) {
        
        int arr[] = {2, 2, 3, 4, 5};
        bubbleSort(arr);

        for (int i : arr) {
            System.out.print(i + " ");                      Output : 1 2 3 4 5 
        }
    }
}
```

### Stable and UnStable Sort

- **`Stable Sort`** ---> If two objects with equal keys appear in the same order in sorted output as they appear in the input data set.  
- **`UnStable Sort`** ---> The order of objects with the same values in the sorted array are not guaranteed to be the same as in the input array.

#### Example 

Array ---> 5 4 3 2 3*

Stable Sort   ---> 2 3 3* 4 5
UnStable Sort ---> 2 3* 3 4 5

> [!NOTE]
> **Bubble Sort is a Stable Sorting Algorithm.**  
> Because it compare only large and small values in arrys.  
> We don't consider eqality in Bubble Sort.  


## Advantages of Bubble Sort:

- Bubble sort is easy to understand and implement.  
- It does not require any additional memory space.  
- It is a stable sorting algorithm, meaning that elements with the same key value maintain their relative order in the sorted output.

## Disadvantages of Bubble Sort:

- Bubble sort has a time complexity of O(n2) which makes it very slow for large data sets.
- Bubble sort has almost no or limited real world applications. It is mostly used in academics to teach different ways of sorting.




































