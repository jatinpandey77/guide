---
title: Storage Class
---
# Storage Classes in C
Storage Classes are used to describe about the features of a variable/function. These features basically include the scope, visibility and life-time which help us to trace the existence of a particular variable during the runtime of a program.

### C language uses 4 storage classes
  * auto
  * extern
  * static
  * register

#### auto
This is the default storage class for all the variables declared inside a function or a block.  Auto variables can be only accessed within the block/function they have been declared and not outside them. 
By default, they are assigned the garbage value by the compiler.

#### extern
The extern storage class is used to give a reference of a global variable that is visible to all the program files.


#### static
Static variables have a property of preserving their value even after they are out of their scope. Hence, static variables preserve the value of their last use in their scope.
By default, they are assigned the value 0 by the compiler.

#### register
The register storage class is used to define local variables that should be stored in a register instead of RAM. This makes the use of register variables to be much faster than that of the variables stored in the memory during the runtime of the program. The register should only be used for variables that require quick access such as counters.
