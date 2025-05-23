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


