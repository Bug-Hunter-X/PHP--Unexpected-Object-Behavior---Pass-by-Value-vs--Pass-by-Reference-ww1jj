# PHP: Unexpected Object Behavior

This repository demonstrates a common, yet subtle, bug in PHP related to object references and their modification within functions.  The core issue involves understanding the difference between passing objects by value and passing them by reference. Incorrect handling can lead to unexpected results, particularly when functions return modified objects.

## Problem
The problem lies in how PHP handles object assignments within functions. While seemingly simple, the implications can be hard to track, especially in larger codebases. 

## Solution
The solution involves understanding the scope of the variable.  The original object remains untouched in `modifyObject`. Explicitly passing by reference using `&` resolves this.  Alternatively, if returning a new object is intended, the return value must be explicitly assigned back to the original variable.

## Files
* `bug.php`: Contains code demonstrating the problematic behavior.
* `bugSolution.php`: Contains code illustrating the corrected behavior.