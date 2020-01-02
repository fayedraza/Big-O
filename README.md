# Big-O


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

ENDFOR

###### Since it will go through every element, so it depends on how long the array is. If the length of an array is one, it will take quickly to go through the array however, if the length is 1000, it will take a lot longer. In addition, it increases linearly as the length of an array increases by 1 its time increases by a bit too.

**Example of an algorithm that has O(n) runtimne (Java)**

public void printString(String s){

for(int x=0; x<s.length(); x++){

System.out.println(s.charAt(x));

}

}

###### Since it is going through every character in the String so it depends on the length of the String which is why the runtime is O(n). It is similar to the array example.

### O(n^2) Runtime

The O(n^2) runtime describes an algorithm that runs in quadratic time. For instance, an algorithm that has an input of 10 runs 100 times.

**Examples of O(n^2) runtime**
- Nested For Loop
- Nested While Loop
- Insertion Sort
- Selection Sort

**Example of an algorithm that has O(n^2) runtimne (Pesudocode)**

READ array

For each row

 For each element in that row

 DISPLAY that element

 ENDFOR

 ENDFOR
 
 ###### Note: Array is n by n 
 
 ###### This is an example of a nested for loop. Since it going through every elment for each array, its run time is O(n^2). If the array length is three rows with three elements it will run nine times. In this case, 3^2 is 9. 
 
 **Example of an algorithm that has O(n^2) runtimne (Java)**
 
 public int returnInt(int n){
 
 int x=0;
 
 while(x<n){
 
 for(int y=0; y<n; y++){
 
 System.out.println(y);
 
 }
 
 x++;
 
 }
 
 }

###### This is an example of a for loop nested under a while loop. Since it is going through every element in the foor loop nested under the while loop, it will take O(n^2) time. 

### O(log n) Runtime

The O(log n) runtime describes an algorithm that runs log n times. Just remember that in computer science when we talk about log n the base is always 2. If an input is 16 then it will run 4 times.

**Examples of O(log n) runtime**
- Binary Search
- Binary Tree

![Binary Search](https://drive.google.com/file/d/1-oHQSTIRbUl-HYlGptDKk-QpkQiyhfgK/view?usp=drivesdk)

###### Start with the top which is 2 and as we choose to go left or right, we are eliminating the other half. For instace, if choose to pick 7 instead of 5 then we will omit 5, 9, and 4.

**Example of an algorithm that has O(log n) runtimne (Pesudocode)**

   READ x
   
   WHILE x is greater than 0
   
   SET x as x divided by 2
   
   ENDWHILE
   
   ###### Look at the number of times the while loop ran. It is dividing by 2 every time it is passed into the while loop meaning that it will run log n times assuming that n is x.
   
   **Example of an algorithm that has O(log n) runtimne (Java)**
    
    public int printNum(int n){
      for (int x = 1; x < n; x = x * 2){
           System.out.println(x);
       }
     }  

###### Look at the number of times the for loop ran. It is multiplying by 2 every time in the for loop meaning that it will run log n times.
    
### O(nlogn) Runtime
    
  The O(log n) runtime describes an algorithm that usually divide and conquer.
  
   **Examples of O(n logn) runtime**
   - Merge sort
   - Heap sort
  
  **Merge Sort Code**
  
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


 ###### Merge sort is a divide a conquer algorithm. More information can be explained about it here.
 
 ### O(2^n) Runtime
 
 The O(2^n) runtime describes an alogrithm whose output doubles as each the input increases.
 
 **Examples of O(2^n) runtime**
 - Fibonacci sequence
 - Towers of Hanoi problem
 
 **Fibonacci Sequence Code**
  
 public static int fibonacci(int num)

{

    if (num <= 1) return num;
    
    return fibonacci(num - 2) + fibonacci(num - 1);

} 
    
### O(n!) Runtime

The O(n!) describes an algortihm that runs n! times.
    
 void nFacRuntimeFunc(int n) {
  for(int i=0; i<n; i++) {
    nFacRuntimeFunc(n-1);
  }
}  
    
### Other Information to Worry About

1. public static void printValues(int a[], int b[]){
    
   for(int x=0; x<a.length; x++){
   System.out.println(a[x]);
   }
   
   for(int x=0; x<b.length; x++){
   System.out.println(b[x]);
   }
   
   }
   
   Sometimes the there can be more than one input that affects the runtime so the runtime can be like O(a+b). In this case, 
   a is the length of one array while b is the length of the other array. Another example is find the length of a 2D array                   where one input is the number of rows and the the other input is the length of each row (assuming the lenght of each 
   row is the same). In this case, the big o is O(ab).     
   
2. The big o runtime O(n^2) can also have different exponents, such as O(n^3) which is slower than O(n^2) runtime. The higher the exponent the slower the runtime.

3. The big O runtime O(2^n) can also be 3^n which are slower.

## Space Complexity 

Space complexity is the measure of how much memory a program is required for execution. 

### Examples of Space Complexity (Assume that this is a 32 bit operating system)

**Example 1: int x= 7;**
 
 The space complexity is O(1) becuase since an int is 4 bytes it will be O(4) which is O(1).
 
 **Example 2: char a= 'x';**
 
 The space complexity is O(1) becuase since an char is 2 bytes it will be O(2) which is O(1).
 
 **Example 3: An Array of Integers**
 
 The space complexity is O(n) becuase we are talking about an integer array that holds many integers. Each integer is 4 bytes         so the space complexity of an array is O(4n) which is O(n).
 
  **Example 4: Linked Lists**
 
 The space complexity is O(n) becuase we are talking about a list that holds many nodes. n represents a node which means it is O(n).
 
  **Example 5:**
  
  public int returnSum(int a[]){
  int x=0;
  
  for(int b =0; b < a.length; b++){
   x += a[b];
   }

  return x;
  
  }
 
 The space complexity is O(n) becuase we are talking about an integer array that holds many integers and two integer variables. Each variable space complexity is O(4). The array space complexity is O(4n) since it is holding a number of integer values. With the space complexity of the method as O(4n + 4 + 4) the 4s get dropped and the constant, 4, also gets dropped which makes the Big O, O(n).
    
    
