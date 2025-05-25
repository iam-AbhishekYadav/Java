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

















