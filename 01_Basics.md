# JAVA 

- **Java** is a high-level, object-oriented programming language used to build applications across platforms—from web and mobile apps to enterprise software.
- Application of **Java** --->

<img src="https://github.com/user-attachments/assets/c6f3cde0-5ff9-4acc-b4b1-4be09149b1d6" alt="Stack1" width="550" height="300">

# # Creating Java File

- FileName.java
- Example ---> Abhi.java

# # Boilerplate Code

``` java
public class FileNmae {
    public static void main(String args[]){

        // <----- Programming ----->
    }
}
```

# # How to Run Java File

**(i)** **`Compile Java File`** ---> javac FileName.java  
**(ii)** **`Run Java File`** ---> javac FileName.java

``` Java
PS D:\Desktop\Java> javac Abhi.java
PS D:\Desktop\Java> java Abhi.java 
Hello World                               // File Run
PS D:\Desktop\Java> 
```

# # Output in Java

- **Syntax** ---> System.out.print("Hello World");

``` java
public class FileNmae {
    public static void main(String args[]){

        System.out.print("Hello World");                  // Output : Hello World
    }
}
```
> [!NOTE]
> For Next Line ---> **println** or **\n**
``` java
System.out.println("Hello World");
System.out.print("Hello World\n");
```

# # Variables in Java

- The name of memory location that we use to store data.
- It is Mutable

<img src="https://github.com/user-attachments/assets/5c4738a0-8cb3-421c-a57b-c57c26810542" alt="Stack1" width="400" height="300">

### Example --->
``` java
public class Abhi {
    public static void main(String args[]){

        int a = 10;
        String name = "Abhishek Yadav";

        System.out.println(a);                   // Output : 10
        System.out.println(name);                // Output : Abhishek Yadav

        a = 69;
        System.out.println(a);                  // Output : 69
    }
}
```

# # Data Types in Java

- It specifies the type of data that the variable can store.

<img src="https://github.com/user-attachments/assets/e98234ba-479b-40c9-97f8-a88f511582e2" alt="Stack1" width="700" height="350">

<br>
<br>
<br>


## 1. Premitive Data Type

- Primitive data store only single values and have no additional capabilities.
- There are 8 primitive data types.

<img src="https://github.com/user-attachments/assets/66a3bb91-635e-45c1-b6af-7d304b71564a" alt="Stack1" width="700" height="400">

## 2. Non-Primitive (Reference) Data Types

- It will contain a memory address of variable values because the reference types won’t store the variable value directly in memory.
- Types of Non-Primitive Data Types.
  - **String**
  - **Array**
  - **Class**
  - **Interfaces**


# # Comments in Java

- **`//`** --> Single Line Comment
- **`/* ----*/`** --> Multi Line Comment

# # Input in Java

- The most common way to take user input in Java is using the Scanner class.
- It is a part of java.util package(collections framework or classes).

### Steps to take user input using Scanner class :-

- Import the Scanner class using **`import java.util.Scanner;`** or **`import java.util.*;`**
- Create the Scanner object and connect Scanner with System.in by passing it as an argument i.e., **`Scanner sc = new Scanner(System.in);`**
- Then use one of Scanner’s handy methods to the response/input :
  - next() for single words
  
<img src="https://github.com/user-attachments/assets/3133df5c-4793-45d8-99a0-123cc57a37df" alt="Stack1" width="500" height="600">

### Example --->
``` java
import java.util.Scanner;
public class Abhi {
    public static void main(String args[]){

        Scanner sc = new Scanner(System.in); 

        String name = sc.next();                   // Input : Abhishek Yadav
        System.out.println(name);                  // Output : Abhishek Yadav
    }
}
```


# # Type Conversion 

- The process of converting data of one data type into another is Known as Type Conversion.
- It is also known as **`Implicit`** or **`Wideninig`** or **`Automatic`** Type Conversion.
- Type Conversion happens when -->
- - The two data types are compatible
  - When we assign a value of a smaller data type to a bigger data type.
 
 
<img src="https://github.com/user-attachments/assets/6d9ba738-c106-4ecb-93ff-835082a2e1ed" alt="Stack1" width="550" height="100">

### Example --->

``` java
import java.util.Scanner;
public class Abhi {
    public static void main(String args[]){

        Scanner sc = new Scanner(System.in);

        float number = sc.nextInt();            // Input : 25
        System.out.println(number);             // Output : 25.0
    }
}
```

# # Type Casting

- If we want to assign a value of a larger data type to a smaller data type we perform Type casting .
- It is also known as **`Explicit`** or **`Narrowing`** Type Casting.
- This is useful for incompatible data types.

<img src="https://github.com/user-attachments/assets/e0ed5421-6161-4d7b-a094-5a430d59be59" alt="Stack1" width="550" height="100">

### Example --->

``` java
import java.util.Scanner;
public class Abhi {
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in); 

        float a = 25.12f;
        
        int b = a;                          // Error: incompatible types: possible lossy conversion from float to int
        int b = (int) a ;

        System.out.println(b);            // Output : 25
    }
}
```

















