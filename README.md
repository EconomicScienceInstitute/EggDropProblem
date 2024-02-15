## Due Date: 3/05 before class
You are allowed to collaborate and use generative AI to write your code.

## Requirements
* Write a file with the solution in a similar format to how we did things in class.
Call it `egg_drop.py`. This file must contain the following:
    * A method named `actions` that takes in a state and returns possible actions
    * A method named `immediate_value` that takes in a state and an action and returns a value
    * A method named `step` that takes in a `state` and an `action` and returns a new state object
    * A function to find the best value and best action. We will call this `egg_drop`. It takes in a state and returns a tuple pair `best_value, best_action` (This was not covered in class. Modifying your code to perform this is an extension.)
* Write a test for each method covering all edge cases you think are necessary to ensure that the function works as intended.
* Use good coding practices to write performant code.

## Problem Description

This is from Geeks 4 Geeks The following is a description of the instance of this famous puzzle involving N = 2 eggs and a building with K = 36 floors. Suppose that we wish to know which stories in a 36-story building are safe to drop eggs from, and which will cause the eggs to break on landing.

We make a few assumptions:

* An egg that survives a fall can be used again.
* A broken egg must be discarded.
* The effect of a fall is the same for all eggs.
* If an egg breaks when dropped, then it would break if dropped from a higher floor.
* If an egg survives a fall then it would survive a shorter fall.  
* It is not ruled out that the first-floor windows break eggs, nor is it ruled out that the 36th-floor does not cause an egg to break. 
* If only one egg is available and we wish to be sure of obtaining the right result, the experiment can be carried out in only one way. 

Drop the egg from the first-floor window; if it survives, drop it from the second-floor window. Continue upward until it breaks. In the worst case, this method may require 36 droppings. Suppose 2 eggs are available.

 What is the least number of egg droppings that are guaranteed to work in all cases?  The problem is not actually to find the critical floor, but merely to decide floors from which eggs should be dropped so that the total number of trials is minimized.

 For instance, Let's say my strategy is to drop it from the 18th floor. If the egg breaks, then I know that the critical floor must be < 18. I now have 17 floors to search and one egg. So worst case scenario the critical floor is 17 and I will need 18 drops to find it. My answer given that strategy is 18. (this is not the correct answer).
 
 Note: In this post, we will discuss a solution to a general problem with ‘N’ eggs and ‘K’ floors
