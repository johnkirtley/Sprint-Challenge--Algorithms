#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) 0(n) 
Initially, the time complexity would be 0(n^3) due to n * n * n. However, we are also multiplying n * n and adding it to a. 


b) O(n log n)
We are iterating through the array once, which is 0(n). While looping through, we are multiplying j * 2, which is cutting the number of iterations it takes to get to n in half.


c) O(n)
The recursive function is being called once on each execution and is decrementing by 1 each time. Therefore, you will proceed in a linear manner.

## Exercise II

To complete this exercise we will utilize a Binary Search function that has a runtime of 0(log n).

Steps:

- Create a variable to hold the number of cracked/dropped eggs. Initially set to 0.
- Create a variable to hold the index value of floor f (the lowest level at which an egg breaks). Initially set to None.
- Write a Binary Search function.
- Check to see if the egg breaks at the middle element.
  - If the egg breaks, increment cracked eggs by 1 and set floor variable to the current index.
    - Since the egg broke at the middle floor, that means we went up too high.
    - To move lower, shift search array to look from the the first floor to middle floor - 1.
    - Call the Binary Search function again with the new search area.
  - Else if egg did not break then we can search higher floors.
    - We can set the search area to the middle floor + 1 to the last floor.
    - Call the Binary Search function again with the new search area.
  - Eventually we will run out of floors to check and will be left with the highest level at which we can drop an egg.

By utilizing Binary Search we only need to drop the egg off of half the floors to get our result.



