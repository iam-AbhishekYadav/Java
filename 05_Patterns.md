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

# # Inverted Half - Pyramid with Numberds

<img src="https://github.com/user-attachments/assets/951eaa21-b51d-4332-8544-22fcda12d2fc"  width="200" height="250">

### Approach for problem solving

- Outer Loop ---> Total No. of Lines (n = 5).
- Number of Rows = **i**
- Last Number of Line = **n - i + 1**
- What to Print ? ---> Numbers (j)

``` java
public class Abhi{
    public static void half_Pyramid_wthNumbers(int n){

        for (int i = 1;  i <= n ; i++) {
            for (int j = 1; j <= n-i+1; j++) {
                System.err.print(j + " ");  
            }
            System.out.println();
        }
    }

    public static void main(String args[]){

        half_Pyramid_wthNumbers(5);
    }
}
```

# # Floyd's Triangle

<img src="https://github.com/user-attachments/assets/1b51cfb2-e956-46f3-9bf0-9444be29eb30"  width="250" height="200">

### Approach for problem solving

- Outer Loop ---> Total No. of Lines (n = 5).
- Number of Rows = **i**
- Counter ---> Increase Numbers
- Number of Rows = Number of Counter
- Inner Loop ---> Track no. of Counter Print

``` java
public class Abhi{
    public static void floyds_triangle(int n){

        int counter = 1 ;

        for (int i = 1;  i <= n ; i++) {
            for (int j = 1; j <= i; j++) {
                System.err.print(counter + " ");

                counter ++;                                
            }
            System.out.println();
        }
    }

    public static void main(String args[]){

        floyds_triangle(5);
    }
}
```

# # 0-1 Triangle

<img src="https://github.com/user-attachments/assets/ea2e3a2e-adf7-4bce-ac0e-57c007902ce4"  width="200" height="250">

<img src="https://github.com/user-attachments/assets/03d4f94a-72a8-4c06-838b-f9181abdc675"  width="200" height="250">

### Approach for problem solving

- Use Matrice approach
- Outer Loop ---> Total No. of Lines (n = 5).
- Number of Rows = **i**
- Number of Column = **j**
- (i + j) = Even ---> 1
- (i + j) = Odd ---> 0

``` java
public class Abhi{ 
    public static void zero_one_triangle(int n){

        for (int i = 1;  i <= n ; i++) {
            for (int j = 1; j <= i; j++) {
                
                if ((i+j) % 2 == 0) {
                    System.out.print("1" + " ");
                } else {
                    System.out.print("0" + " ");
                }                                
            }
            System.out.println();
        }
    }

    public static void main(String args[]){

        zero_one_triangle(5);
    }
}
```











