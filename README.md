# Big O

Click [here](https://github.com/fayedraza/Big-O/blob/master/README.md#space-complexity) for space complexity.

# Time Complexity

### Suppose you want to find the fastest way to get to a store. Which is the best way?   
   - Bus
   - Ask someone to take you
   - Uber
    
### How would you choose the best way?
    The one that is the fastest.
   
### How to measure efficiency of these algorithms?
    Measure the space complexity and the time complexity of the algorithm. These two complexities will be explained later.
    
### What is time complexity?
    The execution time of the algorithm that is denoted by the letter O (Big O).
    
### What is space complexity?
    The amount of space of the algorithm during execution that is denoted by the letter O (Big O).
    
   ![1*j8fUQjaUlmrQEN_udU0_TQ](https://user-images.githubusercontent.com/42160652/71653256-851d7300-2cf9-11ea-9e85-cc1fc52d36a5.jpeg)
   ###### This is a chart showing all of the Big O complexities. The complexities that are horrible are more dominant but slower than the other terms.
    
### Finding the Big O
    
   **Example 1: O(2n+1)**
    
  > O(2n ~~+ 1~~)
  >
  > 1 is dropped since non dominant terms get dropped
  
  > O(~~2~~n)
  >
  > 2 gets dropped since it is a constant
  
  > **Answer: O(n)**
    
   **Example 2: O(n^2+n+1)**
    
   > O(n^2 + n ~~+ 1~~)
   >
   > 1 gets dropped since it is a non dominant term
    
   > O(n^2 ~~+ n~~)
   >
   > n gets dropped since it is a non dominant term
    
   > **Answer: O(n^2)**
    
   **Example 3: O(4)**
     
   > O(~~4~~ 1)
   > Pretend there is 1 behind 4 so we can assume 4 is our constant
   >
   > We can drop the four
   
   > **Answer: O(1)**
   
 ## Big O Runtimes
 
 ### O(1) Runtime
 
 The O(1) Runtime is constant.
 
 **Examples of Java statements with O(1) runtime**
 
 - int x = 7;
 - int b = 27*89;
 - String s = "hi";
 - System.out.println(a[0]); (assume that the array is declared)
 
 **Example of an algorithm that has O(1) runtimne (Pesudocode)**

 >     READ number
 >
 >     DISPLAY number * 3
 
 ###### Despite the value of the number, it will always print that number multiplied by three meaning the time is consant which is why the runtime is O(1).
 
 **Example of a method that has O(1) runtimne (Java)**

```java
 public static void display(int n){
 
    System.out.println(Math.pow(2,n)); // O(1) runtime 
 
    System.out.println(Math.max(2,n)); // O(1) runtime 
 
    System.out.println(Math.ceil(n));  // O(1) runtime 

 }
 ```

###### O(1+1+1) will result to O(3) which is O(1) runtime.

### O(n) Runtime

The O(n) runtime describes an algortihm that increases linearly. The program depends on the size of n.

**Classic examples of O(n) runtime**
- Tranversing through an array
- Tranversing through a link list
- For loop
- While loop

**Example of an algorithm that has O(n) runtimne (Pesudocode)**

>       FOR each element in that array
>
>             DISPLAY that element 
>
>        ENDFOR

###### Since it will go through every element, so it depends upon how long the array is. If the length of an array is one, it will take quickly to go through the array. However, if the length is 1000, it will take a lot longer. In addition, it increases linearly as the length of an array increases by 1 its time increases by a bit too.

**Example of an algorithm that has O(n) runtimne (Java)**

```java
public void printString(String s){

   for(int x=0; x<s.length(); x++){ // O(n) runtime
       System.out.println(s.charAt(x));
   }

}
```

###### Since it is going through every character in the string so it depends upon the length of the string which is why the runtime is O(n). It is similar to the array example.

### O(n^2) Runtime

The O(n^2) runtime describes an algorithm that runs in quadratic time. For instance, an algorithm that has an input of 10 runs 100 times.

**Examples of O(n^2) runtime**
- Nested for loop
- Nested while loop
- [Insertion sort](https://github.com/fayedraza/Algorithms#insertion-sort)
- [Selection sort](https://github.com/fayedraza/Algorithms#selection-sort)

**Example of an algorithm that has O(n^2) runtimne (Pesudocode)**

>      READ array
>
>         For each row
>
>           For each element in that row
>
>           DISPLAY that element
>
>           ENDFOR
>
>         ENDFOR
 
 ###### Note: Array is n by n 
 
 ###### This is an example of a nested for loop. Since it is going through every elment for each row, its run time is O(n^2). If the array length is three rows with three elements in each row then it will run nine times because 3^2 is 9. 
 
 **Example of an algorithm that has O(n^2) runtimne (Java)**
  
 ``` java
   public int returnInt(int n){
 
     int x=0;
      while(x<n){
         for(int y=0; y<n; y++){
            System.out.println(y);
         }
                x++;
       }
 
    }
 ```
 
###### This is an example of a for loop nested under a while loop. Since it is going through every element in the foor loop nested under the while loop, it will take O(n^2) time. 

### O(log n) Runtime

The O(log n) runtime describes an algorithm that runs log n times. Just remember that in computer science when we talk about log n the base is always 2. If an input is 16 then it will run 4 times.

**Examples of O(log n) runtime**
- [Binary search](https://github.com/fayedraza/Algorithms#binary-search)
- Binary tree

![ya+FtimvfAAAAABJRU5ErkJggg==](https://user-images.githubusercontent.com/42160652/71653678-c7e04a80-2cfb-11ea-9ad1-2d67300eb442.png)

###### This is a binary tree. Starting at the top which is 2 and as we choose to go left or right, we are eliminating the other half. For instace, if we choose to pick 7 instead of 5 then we will omit 5, 9, and 4.

**Example of an algorithm that has O(log n) runtimne (Pesudocode)**

  >      READ x
  > 
  >        WHILE x is greater than 0
  > 
  >           SET x as x divided by 2
  >
  >        ENDWHILE
  
   ###### Look at the number of times the while loop ran. It is dividing by 2 every time it is passed into the while loop meaning that it will run log n times assuming that n is x.
   
   **Example of an algorithm that has O(log n) runtime (Java)**
    
``` java
 public int printNum(int n){
      
  for (int x = 1; x < n; x = x * 2){
       System.out.println(x);
  }
       
}  
 ``` 

###### Look at the number of times the for loop ran. It is multiplying by 2 every time in the for loop meaning that it will run log n times.
    
### O(nlog n) Runtime
    
  The O(nlog n) runtime describes a divide and conquer algorithm.
  
   **Examples of O(nlog n) runtime**
   - [Merge sort](https://github.com/fayedraza/Algorithms/blob/master/README.md#merge-sort)
   - Heap sort
  
  **Merge Sort Code**

``` java
public static void sort (int []a, int lo, int hi){

   int n = hi-lo;

   if(n<=1)
      return;
  
     int middle = lo + n/2;
  
     sort(a, lo, middle);
     sort(a, middle, hi);
     merge(a,lo,middle,hi);
 
 }
 
public static void merge(int []a, int lo, int mid, int hi){

   int i=lo;
   int j=mid;
   int n= hi-lo;

   for(int k=0; k<n; k++){

       if(i==mid)
         aux[k] = a[j++];
       else if (j==hi)
         aux[k] = a[i++];
       else if (a[j] < a[i])
         aux[k] = a[j++];
       else
         aux[k] = a[i++];
         
   }
``` 

![IMG_2519](https://user-images.githubusercontent.com/42160652/71680074-2b4b9600-2d57-11ea-9b18-53a855ac71af.jpeg)

 ###### As shown above, merge sort is a divide and conquer algorithm.
 
 ### O(2^n) Runtime
 
 The O(2^n) runtime describes an alogrithm whose output doubles as the input increases.
 
 **Examples of O(2^n) runtime**
 - Fibonacci sequence
 - [Towers of Hanoi problem](https://www.geeksforgeeks.org/java-program-for-tower-of-hanoi/)
 
 **Fibonacci Sequence Code (Java)**
  
 ``` java 
 public static int fibonacci(int num) {

    if (num <= 1) 
      return num;
    
    return fibonacci(num - 2) + fibonacci(num - 1);

} 
``` 
 
![IMG_2520](https://user-images.githubusercontent.com/42160652/71681600-17099800-2d5b-11ea-895f-17e880646388.jpeg)

###### Note: fib is short for fibonacci

###### As shown above, the output doubles each time. It doubles from 2 to 4 to 8. This is why the runtime is O(2^n).

### O(n!) Runtime

The O(n!) describes an algortihm that runs n! times.

 **Example of an algorithm that has O(n!) runtimne (Java)**
 
 ``` java 
 public void printFactorial(int n) {
  
    if(n == 0)
      return;
  
  int x=0;
  while (x<n){
    System.out.print(n)
    x++;
   } 

 System.out.println(); 
 nFacRuntimeFunc(n-1);
  
 }  
 ``` 
 
![IMG_2570](https://user-images.githubusercontent.com/42160652/72012222-8e429e80-3229-11ea-9193-4067d320921a.jpeg)

### Other Information to Worry About

1. 

``` java
public static void printValues(int a[], int b[]){
    
   for(int x=0; x<a.length; x++){ //O(a)
   System.out.println(a[x]);
   }
   
   for(int x=0; x<b.length; x++){ //O(b)
   System.out.println(b[x]);
   }
   // O(a + b)
   
 }
 ``` 
 
   Sometimes there can be more than one input that affects the runtime so the runtime can be like O(a + log b). In this case, a is the length of one array while b is the length of the other array. Both for loops do not affect each other so the      runtime is O(a+b). Another example is finding the sum of a 2D array where one input is the number of rows and the other input is the length of each row (assuming that a and b are not the same value). In this case, the Big O is O(ab).     
   
2. 

``` java
public static void printValues(int x, int y, int z){
  
    for(int a=0;a<x;x++){ // O(n)
      for(int b=0; b<y; b++){ // O(n)
       for(int c=0; c<z; c++){ // O(n)
         System.out.println(a+b+c);
                              }
                   }
         }
         // O(n*n*n)-> O(n^3)
         
 }        
``` 

The Big O runtime O(n^2) can also have different exponents, such as O(n^3) which is slower than O(n^2) runtime. The higher the exponent the slower the runtime. An example is a triple nested for loop.

3. 

The Big O runtime O(2^n) can also have a different base, such as 3^n which is slower than 2^n. The higher the base the slower the runtime.

# Space Complexity 

###### Click [here](https://github.com/fayedraza/Big-O/blob/master/README.md#time-complexity) for time complexity.

Space complexity is the measure of how much memory a program is required for execution.

![IMG_2518](https://user-images.githubusercontent.com/42160652/71678987-7adc9280-2d54-11ea-9daf-6e0d8acb4477.jpeg)
###### Typical memory used by primitive types

### Examples of Space Complexity (Assume that we are using the chart above)

Please be advised it covers topics discussed earlier. Click [here](https://github.com/fayedraza/Big-O/blob/master/README.md#finding-the-big-o) to review the topic.

**Example 1: int x= 7;**
 
 The space complexity is O(1) since an int is 4 bytes so it will be O(4) which is O(1).
 
 **Example 2: char a= 'x';**
 
 The space complexity is O(1) since a char is 2 bytes so it will be O(2) which is O(1).
 
 **Example 3: An Array of Integers**
 
 The space complexity is O(n) becuase we are talking about an integer array that holds many integers. Each integer is 4 bytes so the space complexity of an array is O(4n) which is O(n).
 
  **Example 4: Linked Lists**
 
 The space complexity is O(n) becuase we are talking about a list that holds many nodes. n represents a node which means it is O(n).
 
  **Example 5:**
  
  ```java
  public int returnSum(int a[]){
      int x=0;
  
     for(int b =0; b < a.length; b++){
         x += a[b];
     }

    return x;
  
  }
  ```
 
 The space complexity is O(n) becuase we are talking about an integer array that holds many integers and two integer variables. Each variable space complexity is O(4). The array space complexity is O(4n) since it is holding a number of integer values. With the space complexity of the method as O(4n + 4 + 4) the 4s get dropped and the constant, 4, also gets dropped which makes the Big O, O(n).
    
    
