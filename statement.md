# description: 
 The 2nd and 3rd operands to the conditional operator must be of the same type.  If one of the two can be converted to the other, the conversion will occur.  Note: if a conversion exists for each of the operands into the other's type, the program is ill-formed.
```C++ runnable
#include <iostream>

struct Foo
{
  int x;

  operator int()
  {
    return 21;
  }
};

int main(int argc, char** argv)
{
  Foo f;
  f.x = 11;

  std::cout << (0?3:f) << std::endl;

  return 0;
}
