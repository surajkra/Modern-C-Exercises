## Constexpr

Constant Expressions are a part of C++ already. Example would be 1+2, 3*4. Such expressions always produce the same result without any side effects. If the compiler can directly optimze these at compile time, it increases the performance of the program. 

In the exercise, we see different ways of defining variables and most improtantly using constexpr. Using *const* creates a *const* Constant and not a Constant Expression. C++11 uses constexpr for this regard. Any array length during definition must be based on a constant expression and not a *const* constant, which is why the following code is Illegal, 

```cpp
const int len = 10;
constexpr int len_2 = 1 + 9;
char arr_1[len]; //Illegal
char arr_2[len_2]; //Legal
```

C++11 provides constexpr to let the user explicitly declare that the function or object constructor
will become a constant expression at compile time.

In addition, constexpr function can use simple statements like local variables, loops and branches internally in C++14 (just like any other method). Whereas in C++11 this is not allowed and should always follow a single line return. 
