# # Patterns Printing Questions

# # Square Pattern

<img src="https://github.com/user-attachments/assets/dda082db-0303-45bb-99dc-f873e6e0b20c"  width="200" height="200">

``` java
public class Abhi{
    public static void main(String args[]){
        
        // for (int line = 1; line <= 4; line++) {
        //     System.out.println("****");
        // }

        int l = 1;
        while (l<=4) {
            System.out.println("****");
            l++;
        }
    } 
}
```

# # Star Pattern

<img src="https://github.com/user-attachments/assets/fcdf5557-b55a-4635-b0e9-13b06f270c47"  width="200" height="200">

### Approach for problem solving

- Outer Loop ---> No. of Lines (4) 
- Inner Loop ---> No. of times Char Print 
- What to Print ? ---> **`*`**

``` java
public class Abhi{
    public static void main(String args[]){
 
        for (int line = 1;  line <= 4; line++) {
            for (int star = 1; star <= line; star++) {
                System.err.print("*");
            }
            System.out.println();                        // For Next Line
        }
    } 
}
```

# # Inverted - Star Pattern

<img src="https://github.com/user-attachments/assets/e225a649-460d-479d-bffa-d92fd8e9b8fd"  width="200" height="200">

### Approach for problem solving

- Outer Loop ---> No. of Lines (4)
- Inner Loop ---> Star = **n - Line + 1** 

``` java
public class Abhi{
    public static void main(String args[]){

        int n = 4;                                  // n = No. of lines
        
        for (int line = 1;  line <= n ; line++) {
            for (int star = 1; star <= (n-line+1); star++) {
                System.err.print("*");
            }
            System.out.println();
        }
    } 
}
```

# # Half - Pyramid Pattern

<img src="https://github.com/user-attachments/assets/1f3b7f2a-338d-4212-ba45-fdbb2fe6de51"  width="200" height="250">

### Approach for problem solving

- Outer Loop ---> No. of Lines (4) 
- Inner Loop ---> Inner Loop runs = No. of Lines
- What to Print ? ---> Inner Loop Count

``` java
public class Abhi{

    public static void main(String args[]){
        
        for (int line = 1;  line <= 4 ; line++) {
            for (int number = 1; number <= line; number++) {
                System.err.print(number);
            }
            System.out.println();
        }
    } 
}
```

# # Character Pattern

<img src="https://github.com/user-attachments/assets/112cba91-6daf-490c-a3b0-15ebe65bbe9d"  width="200" height="250">

### Approach for problem solving

- Outer Loop ---> No. of Lines (4) 
- Inner Loop ---> Char Count = No. of Lines
- What to Print ? ---> Increace char every time

``` java
public class Abhi{
    public static void main(String args[]){

        char ch = 'A';

        for (int line = 1;  line <= 4 ; line++) {
            for (int number = 1; number <= line; number++) {

                System.err.print(ch);
                ch ++;                                // For increasing char.
            }
            System.out.println();
        }
    } 
}
```

# # Hollow Rectange Pattern

<img src="https://github.com/user-attachments/assets/8c0373f9-9458-42eb-b708-a7f5d0a9effb"  width="200" height="200">
<img src="https://github.com/user-attachments/assets/34e32868-b72d-440b-aeec-c379ee1727e5"  width="200" height="200">

### Approach for problem solving

- Use Matrice to solve.
- Boundary ---> **Row = 1 or 4**  and **Column = 1 or 5**
- Outer Loop ---> Total Lines (Rows)
- Inner Loop ---> Total Columns 
- What will be printed inside each line ---> Check Condition
  - Row = 1 || Col = 1 || Row = 4 || Col = 5
 
``` java
public class Abhi{ 
    public static void hollow_Rect(int totRows, int totCols) {

        for (int i=1; i<=totRows; i++) {
                for (int j=1; j<=totCols ; j++) {

                    if (i == 1 || i == totRows || j == 1  || j == totCols) {            // Cell - (i,j)
                        System.out.print("*");
                    } else{
                        System.out.print(" ");
                    }
                }
                System.out.println();
            }  
        }
        
    public static void main(String args[]){

        hollow_Rect(4,5);
    }
}
```

# # Inverted & Rotated Half - Pyramid

<img src="https://github.com/user-attachments/assets/12bb5958-b1d2-4da7-9389-f652eda1cd3b"  width="200" height="200">

### Approach for problem solving

- Outer Loop ---> Total No. of Lines (n = 4).
- What will be printed in each line ---> **Spaces + Stars**
- No. of Rows (i) = Stars
- No. of Spaces = **n-i**

``` java
public class Abhi{
    public static void half_Pyramid(int n) {

        for (int i = 1; i <= n; i++) {                               // Outer Loop

            for (int j = 1; j <= n-i; j++) {                        // For Spaces
                System.out.print(" ");
            }

            for (int j = 1; j <=i ; j++) {                           // For Stars

                System.out.print("*");
            }

            System.out.println();
        }    
    }
    public static void main(String args[]){

        half_Pyramid(4);
    }
}
```






 














