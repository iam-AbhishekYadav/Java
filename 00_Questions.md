# Questions

# # Count the numbers of digits for a given number n.

### Approach to Solve a problem

- Divide n by 10 until &nbsp;**n > 0** &nbsp; &nbsp;---> Integer Division
- **n/10** ---> Removes the last digit
- Count the number of Division.
- Loop Termination ---> **n > 0**

``` java
import java.util.*;
public class Abhi {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();                    // Input : 12345678
        int numOfDigits = 0;
        int originalNmber = n;

        while (n > 0) {
            n = n/10;

            numOfDigits ++;
        }
        System.out.println("Number of digits in " + originalNmber + "=" + numOfDigits);          // Output : Number of digits in 12345678 = 8
    }
}
```

# # Find the sun of digits in a given number n.

### Approach to Solve a problem

- Modulo n by 10 = Last digit of number(n)
- Divide n by 10 until &nbsp;**n > 0** &nbsp; &nbsp;---> Integer Division
- **n/10** ---> Removes the last digit
- Add Last digit of number in Answer &nbsp; &nbsp;---> **Ans += n % 10**
- Loop Termination ---> **n > 0**

``` java
import java.util.*;
public class Abhi {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();                    // Input : 12345
        int sumOfDigits = 0;
        int originalNmber = n;

        while (n > 0) {
            sumOfDigits += n%10;
            n = n/10;
        }
        System.out.println("Sum of digits in " + originalNmber + "=" + sumOfDigits);          // Output : Sum of digits in 12345 = 15
    }
}
```

# Reverse the digits of a given number n.

### Approach to Solve a problem

<img src="https://github.com/user-attachments/assets/f313f96b-2b1c-443b-8995-7b9c53940054" width="350" height="200">

- **Answer = Old_Ans * 10 + n % 10**
- n % 10 = Last digit of number(n)
- Loop Termination ---> **n > 0**

``` java
import java.util.*;
public class Abhi {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();                    // Input : 12345
        int reversefDigits = 0;
        int originalNmber = n;

        while (n > 0) {
            reversefDigits = reversefDigits * 10 + n%10;
            n = n/10;
        }
        System.out.println("Reverse of digits is " + originalNmber + "=" + reversefDigits);          // Output : Reverse of digits in 12345 = 54321
    }
}
```





























