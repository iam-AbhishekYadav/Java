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

- No. of Lines(4) ---> Outer Loop
- No. of times Char Print ---> Inner Loop
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










 














