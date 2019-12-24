# Big-O


### Suppose you want to find the fastest way to get to a store. Which is the best way?   
   - Bus
   - Ask someone to take you
   - Uber
    
### How would you choose the best way?
    The one that is the fastest
   
### How to measure efficiency of these algorithms?
    Measure the space complexity and the time complexity of the algorithm. These two complexities will be explained later.
    
### What is time complexity?
    The execution time of the algorithm that is denoted by the letter O (Big O).
    
### What is space complexity?
    The amount of space of the algorithm that is denoted by the letter O (Big O).
    
### Finding the Big O
    
   **Example 1: O(2n+1)**
    
   O(2n ~~+ 1~~)
   1 is dropped since non dominant terms get dropped
    
   O(~~2~~n)
   2 gets dropped since it is a constant
    
   Answer: O(n)
    
   **Example 2: O(n^2+n+1)**
    
   O(n^2 + n ~~+ 1~~)
   1 gets dropped since it is a non dominant term
    
   O(n^2 ~~+ n~~)
   n gets dropped since it is a non dominant term
    
   Answer: O(n^2)
    
   **Example 3: O(4)**
     
   O(1)
   Since it is a number it is almost the same time complexity as O(1)
     
   Answer: O(1)
   
 ## Big O Runtimes
 
 ### O(1) Runtime
 
 The O(1) Runtime is constant.
 
 **Examples of Java statements with O(1) runtime**
 
 - int x = 7;
 - int b = 27*89;
 - String s = "hi";
 - System.out.println(a[0]); (assume that array is declared)
 
 **Example of an algorithm that has O(1) runtimne (Pesudocode)**

 READ number
 
 DISPLAY number * 3
 
 ###### Despite the number it will always print that number multiplied by three meaning the time is consant which also means the runtime is O(1)
 
 **Example of a method that has O(1) runtimne (Java)**

 public static void display(int n){
 
 System.out.println(Math.pow(2,n)); - O(1) runtime 
 
 System.out.println(Math.max(2,n)); - O(1) runtime 
 
 System.out.println(Math.ceil(n));  - O(1) runtime 

 }
 
###### O(1+1+1) will result to O(3) which is O(1) runtime

### O(n) Runtime

The O(n) runtime describes an algortihm that increases linearly. The program depends on the size of n.

**Classic examples of O(n) runtime**
- Tranversing through an array
- Tranversing through a link list
- for loop
- while loop

**Example of an algorithm that has O(n) runtimne (Pesudocode)**

FOR each element in that array
DISPLAY that element 

###### Since it will go through every element so it depends on how long the array is. If the length of an array is 1 it will take quickly to go through the array however if the length is 1000 it will take a lot longer. In addition, it increases linearly since as the length of an array increases by 1 its time increases too.

**Example of an algorithm that has O(n) runtimne (Java)**

public void printString(String s){

for(int x=0; x<s.length(); x++){
System.out.println(s.charAt(x));
}

}

###### Since it is going through every character in the String so it depends on the length of the String which is why the runtime is O(n). It is similar to the array example.

    
    
    
    
    
    
    
    
    
    
    
