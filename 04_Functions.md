 # # Functions or Methods

- **Java** Methods are blocks of code that perform a specific task.
- A method allows us to reuse code, improving both efficiency and organization.
- All methods in Java must belong to a class.

# # Syntax

<img src="https://github.com/user-attachments/assets/ccdbed11-caa6-48b2-bdb1-cd0fc9e19f5b" alt="Stack1" width="600" height="350">


### Key Components of a Method Declaration

- **`Modifier`** : It specifies the method's access level (e.g., public, private, protected, or default).
- **`Return Type`** : The type of value returned, or void if no value is returned.
- **`Method Name`** : It follows Java naming conventions; it should start with a lowercase verb and use camel case for multiple words.
- **`Parameters`** : A list of input values (optional). Empty parentheses are used if no parameters are needed.
- **`Method Body`** : It contains the logic to be executed (optional in the case of abstract methods).

### Example 1 --->

``` Java
public class Abhi {
    public static void printMessage(){
        System.err.println("Hello My name is Scahin");

        return ;
    }
    public static void main(String args[]){

        printMessage();                          // Function Call      // Output : Hello My name is Scahin
    }
}
```

### Example 2 ---> With Parameters

``` Java
import java.util.*;
public class Abhi {
    public static int calulateSum(int num1 , int num2){         // Parameters or Formal Parametes
        int sum = num1 +num2;
        return sum;
    }
    public static void main(String args[]){

        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();                         // Input : 2
        int b = sc.nextInt();                         // Input : 5
        int sum = calulateSum(a, b);                  // Arguments or Actual Parameters

        System.err.println("Sum is :" +sum);         // Output : 7
    }
}
```

# # Call by Value in Java

- A copy of actual parameters is passed into formal parameters.
- Changes in formal parameters will not result in changes in actual parameters.
- Separate memory location is allocated for actual and formal parameters.
- **Java is always calls by value.**

### Example 1 ---> Swap - Values Exchange

``` java
public class Abhi {
    public static void main(String args[]){
        int a = 5;
        int b = 10;

        int temp = a;
        a = b ;
        b = temp ;

        System.err.println("a = " +a);          // Output : a = 10
        System.err.println("b = " +b);          // Output : b = 5
    }
}
```
**1**
<img src="https://github.com/user-attachments/assets/aa453022-2c57-4add-9499-c1d617a17ff6" alt="Stack1" width="350" height="600">
**2**
<img src="https://github.com/user-attachments/assets/941733f5-8d7d-46dd-9573-c4809de01e7a" alt="Stack1" width="350" height="600">


### Example 1 ---> Swap in Function

``` java
public class Abhi {
    public static void swap(int a,int b){
        int temp = a;
        a = b ;
        b = temp ;

        System.err.println("a = " +a);                     // Output : a = 10
        System.err.println("b = " +b);                     // Output : b = 5

    }
    public static void main(String args[]){
        int a = 5;
        int b = 10;

        swap(a,b);

        // System.err.println("a = " +a);                     // Output : a = 5
       //  System.err.println("b = " +b);                     // Output : a = 10
    }
}
```

# # Types of Functions / Methods

**-->** There are two types of Function in Java.

### 1. Predefined Method  

- The method that is already defined in the Java class libraries.
- It is also known as the standard library method or built-in method.

**Ex -->** random() , Math() , sc.nextInt() ....etc.

### 2. User-defined Method  

- The method written by the user or programmer.
- These methods are modified according to the requirement.

**Ex -->** sum , factorial , product ....etc.

# # Function Overloading

- Multiple function with the same name but different parameters within a class.
- Overloading does not depend on the return type of the method, two methods cannot be overloaded by just changing the return type.

## Different Ways of Method Overloading in Java

**1. Changing the Number of Parameters**

``` java
public class Abhi {
    public static int sum(int a,int b){

        int sum = a + b ;
        return sum ;
    }

    public static int sum(int a,int b,int c){

        int sum = a + b + c;
        return sum ;
    }
    public static void main(String args[]){

        System.err.println(sum(5, 4));                       // Output : 9
        System.err.println(sum(5, 4, 3));                    // Outpot : 12
    }
}
```

**1. Changing Data Types of the Arguments**

``` java
public class Abhi {
    public static int sum(int a,int b){

        int sum = a + b ;
        return sum ;
    }

    public static float sum(float a,float b){

        float sum = a + b ;
        return sum ;
    }
    public static void main(String args[]){

        System.err.println(sum(5, 4));                           // Output : 9
        System.err.println(sum(5f, 4.3f));                       // Output : 9.3
    }
}
```

# # Binary Number System

- Binary number is a number expressed in the base 2 numeral system.
- Binary number's digits have 2 symbols: zero (0) and one (1).
- Each digit of a binary number counts a power of 2.

**Ex -->** 1101<sub>2</sub> =  1 × 2<sup>3</sup> + 1 × 2<sup>2</sup> + 0 × 2 <sup>1</sup> + 1 × 2 <sup>0</sup>

# # Decimal Number Sysytem

- Decimal number is a number expressed in the base 10 numeral system.
- Decimal number's digits have 10 symbols: 0,1,2,3,4,5,6,7,8,9.
- Each digit of a decimal number counts a power of 10

**Ex -->** 653<sub>10</sub> = 6 × 10<sup>2</sup> + 5 × 10<sup>2</sup> + 3 × 10<sup>0</sup>


# # Convert From Binary to Decimal

- For binary number with n digits : -->  
> **d<sub>n-1</sub> ... d<sub>3</sub> d<sub>2</sub> d<sub>2</sub> d<sub>0</sub>**
- The decimal number is equal to the sum of binary digits (dn) times their power of 2 (2n):
> Decimal = d<sub>0</sub> x 2<sup>0</sup> + d<sub>1</sub> x 2<sup>1</sup> + d<sub>2</sub> x 2<sup>2</sup> ....

**Ex -->** 1101<sub>2</sub> =  1 × 2<sup>3</sup> + 1 × 2<sup>2</sup> + 0 × 2 <sup>1</sup> + 1 × 2 <sup>0</sup> = 13<sub>10</sub>

<img src="https://github.com/user-attachments/assets/85a4c74c-3f9e-4c83-ae96-c371f5c64f50" alt="Stack1" width="450" height="250">

### Code for Conversion

``` java
public class Abhi {
    public static void binTodec(int binNum){
        int myNum = binNum;
        int pow = 0;
        int decNum = 0;

        while (binNum>0) {
            int lastDigit = binNum % 10;
            decNum = decNum + (lastDigit * (int)Math.pow(2, pow));

            pow ++;
            binNum = binNum/10;
        }
        System.out.println("Decimal of "+ myNum +"=" +decNum);
    }
    public static void main(String args[]){

        binTodec(1001);                                            // Output : Decimal of 1001 = 9
    } 
}
```

# # Convert From Decimal to Binary

### Conversion steps:

**1.** Divide the number by 2.  
**2.** Get the integer quotient for the next iteration.  
**3.** Get the remainder for the binary digit.  
**4.** Repeat the steps until the quotient is equal to 0.  

<img src="https://github.com/user-attachments/assets/7f4dc1d8-4905-4657-92ca-cfb5052ba3f1" alt="Stack1" width="350" height="250">


### Code for Conversion

``` java
public class Abhi {
    public static void decTobin(int n){
        int myNum = n;
        int pow = 0;
        int binNum = 0;

        while (n>0) {
            int rem = n % 2;
            binNum = binNum + (rem * (int)Math.pow(10,pow));

            pow ++;
            n = n/2;
        }
        System.out.println("Binary of "+ myNum +"=" +binNum);
    }
    public static void main(String args[]){

        decTobin(9);                                          // Output : Binary of 9 = 1001
    } 
}
```

# # Scope in Java

- In Java, variables are only accessible inside the region they are created. This is called scope.

## Method Scope

- Variables declared directly inside a method are available anywhere in the method following the line of code in which they were declared:

## Block Scope

- A block of code refers to all of the code between **curly braces {}**.
- Variables declared inside blocks of code are only accessible by the code between the curly braces, which follows the line in which the variable was declared:










