## nullptr

C++ does not allow to implicitly convert void * to other types.

C++ without the void * implicit conversion has to define NULL as 0. This still creates a new problem. Defining NULL to 0 will cause the overloading feature in C++ to be confusing. Consider the following two foo functions:
void foo(char*);
void foo(int);
Then the foo(NULL); statement will call foo(int), which will cause the code to be counterintuitive.

To solve this problem, C++11 introduced the nullptr keyword, which is specifically used to dis-tinguish null pointers, 0. The type of nullptr is nullptr_t, which can be implicitly converted to any pointer or member pointer type, and can be compared equally or unequally with them.

The code uses overloaded functions to show the solution with C++11, to differentiate these types. 

In essence, NULL is different fromn 0 and nullptr. 