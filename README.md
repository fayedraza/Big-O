# Big-O


### Suppose you want to find the fastest way to get to a store. Which is the best way?   
    - Bus
    - Ask someone to take you
    - Uber
    
### How would you choose the best way?
    - the one that is the fastest
   
### How to measure efficiency of these algorithms?
    Measure the space complexity and the time complexity of the algorithm. These two complexities will be explained later.
    
### What is time complexity?
    The execution time of the algorithm that is denoted by the letter O (Big O).
    
### What is space complexity?
    The amount of space of the algorithm that is denoted by the letter O (Big O).
    
### Finding the Big O
    
    _Example 1_: # O(2n+1)
    
    O(2n)
    1 is dropped since non dominant terms get dropped
    
    O(n)
    2 gets dropped since it is a constant
    
    _Answer:_ O(n)
    
    _Example 2:_ O(n^2+n+1)
    
    O(n^2+n)
    1 gets dropped since it is a non dominant term
    
    O(n^2)
    n gets dropped since it is a non dominant term
    
     _Answer:_ O(n^2)
    
     _Example 3:_ O(4)
     
     O(1)
     Since it is a number it is almost the same time complexity as O(1)
     
     _Answer:_ O(1)
    
    
    
    
    
    
    
    
    
    
    
