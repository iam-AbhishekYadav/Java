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

# # Print the first n factorial numbers.

### Approach to Solve a problem

- **factorial = factorial * i**

``` java
import java.util.*;
public class Abhi {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();                    // Input : 5
        int fact = 1;

        for (int i = 1; i <=n; i++) {
            fact = fact * i;
        }
        System.out.println(fact);                // Output : 120
    }
}
```

# # Find the sun of the following series ---> S = 1 - 2 + 3 - 4 ....n

### Approach to Solve a problem

- Odd Numbers ---> **+ve**
- Even Numbers ---> **-v**
- If Odd add 1
- If Even substract 1

``` java
import java.util.*;
public class Abhi {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();                    // Input : 5
        int sum = 0;

        for (int i = 1; i <=n; i++) {
            if (i % 2 == 0) {
                sum -= i;
            } else {
                sum += i;
            }
        }
        System.out.println(sum);                  // Output : 3
    }
}
```

# Given 2 numbers a and b , Find a raise to power b.

### Approach to Solve a problem

- Outer loop ---> Run b - times
- **Answer = Ans * a**

``` java
import java.util.*;
public class Abhi {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt() , b = sc.nextInt();                    // Input : a = 2 , b = 5
        int ans = 1;

        for (int i = 1; i <=b; i++) {
            ans = ans * a ;
        }
        System.out.println(ans);                  // Output : 32
    }
}
```






























































