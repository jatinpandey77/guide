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
This is the default storage class for all the variables declared inside a function or a block.  Auto variables can be only accessed within the block/function they have been declared and not outside them. Of course, these can be accessed within nested blocks within the parent block/function in which the auto variable was declared. However, they can be accessed outside their scope as well using the concept of pointers given here by pointing to the very exact memory location where the variables resides. They are assigned a garbage value by default whenever they are declared.

#### extern
The extern storage class is used to give a reference of a global variable that is visible to all the program files.
Basically, the value is assigned to it in a different block and this can be overwritten/changed in a different block as well. So an extern variable is nothing but a global variable initialized with a legal value where it is declared in order to be used elsewhere. It can be accessed within any function/block. Also, a normal global variable can be made extern as well by placing the ‘extern’ keyword before its declaration/definition in any function/block. This basically signifies that we are not initializing a new variable but instead we are using/accessing the global variable only. The main purpose of using extern variables is that they can be accessed between two different files which are part of a large program. For more information on how extern variables work, have a look at this link.

#### static
Static variables have a property of preserving their value even after they are out of their scope. Hence, static variables preserve the value of their last use in their scope. So we can say that they are initialized only once and exist till the termination of the program. Thus, no new memory is allocated because they are not re-declared. Their scope is local to the function to which they were defined. Global static variables can be accessed anywhere in the program. By default, they are assigned the value 0 by the compiler.

#### register
The register storage class is used to define local variables that should be stored in a register instead of RAM. 
This storage class declares register variables which have the same functionality as that of the auto variables. This makes the use of register variables to be much faster than that of the variables stored in the memory during the runtime of the program. If a free register is not available, these are then stored in the memory only. The register should only be used for variables that require quick access such as counters.
