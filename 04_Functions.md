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

### Example --->

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

