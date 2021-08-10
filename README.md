# Korbolko C++ Coding Style Guide

This guide contains the spelling rules to be followed when coding.

## Naming

-   This area covers the naming of various items to be used in programming.
-   The notations used in naming are given below.

| Format    | Name                        | Usages                                                  |
| :-------- | :-------------------------- | :------------------------------------------------------ |
| our_words | underscore                  | Naming the file.                                        |
| ourWords  | lowerCamelCase              | Variables, Functions/Methods .. etc.                    |
| OurWords  | UpperCamelCase / PascalCase | Class, Struct, Namespace, Enum and Enum Members .. etc. |
| OURWORDS  | UPPERCASE                   | Constant Literals, Macros .. etc.                       |
| OUR_WORDS | MACRO_CASE                  | Constant Literals, Macros .. etc.                       |

### Naming Files :

The C++ header file can have extensions such as .h, .hh, .hpp, .hh or .hxx. It's recommended that a user-defined header file have the .hpp extension. Underscore will be used when separating file names.

```txt
; Header Files

file.hpp                        ///< OK
my_file.hpp                     ///< OK
adventure_game.hpp              ///< OK


; Source Files

file.cpp                        ///< OK
my_other_files.cc               ///< OK


; --------------------------------------

MyFile.cpp                      ///< INCORRECT
my-code.cpp                     ///< INCORRECT
myExampleFile.cpp               ///< INCORRECT
```

> While user-defined data types are named with the "UpperCamelCase" method, functions(or methods) and primitive data types are named with the "lowerCamelCase" method.

### Naming User Defined Data Types:

```cpp
///< class names
class MyClass;                  ///< OK

class MyAnotherClass;           ///< OK

///< struct names
struct MyStruct;                ///< OK

struct MyAnotherStruct;         ///< OK

///< namespaces
namespace Example {}            ///< OK

///< enum class names
enum class MyEnum {}            ///< OK
enum class MyEnumStyle {}       ///< OK

///< ---------------------------------------

class myGameClass;              ///< INCORRECT
class my_example_class;         ///< INCORRECT

enum colors {};                 ///< INCORRECT
```

### Naming User-Defined Fuctions/Methods

-   "loweCamelCase" style will be used in parameter naming.

```cpp
void myFunction(/* params */);                  ///< OK
double func(int myParam, double dbVar);         ///< OK
```

### Naming Variables:

```cpp
///< using with primitive data types

int myVariable;             ///< OK
float myfloatNum;           ///< OK
std::string str;            ///< OK

///< A better solution is to align the identifiers.

int             myVariable;
float           myfloatNum;
std::string     str;       

///< using with user defined types

class MyClass {};
///< . . .
///< . . .
MyClass myObj;


enum class MyColor { Red, Green, Blue };
///< . . .
///< . . .
MyColor myFavoriteColor = MyColor::Red;         ///< OK

///< naming class and struct members : this is same to variable naming;

class Another;
class MyExampleClass
{
public:
    Another     myExampleClass;                 ///< OK
    std::string classMember;                    ///< OK
};  

struct MyStruct
{
    int     myStructVar                         ///< OK

    int     ExampleVar                          ///< INCORRECT
    char    another_example                     ///< INCORRECT
};

///< Enums
enum class Color { Red, Green, Blue };          ///< OK
enum class Color { RED, GREEN, BLUE };          ///< OK

enum class Library
{  
    PROGRAMMİNG_BOOKS,                          ///< OK
    ComicBooks,                                 ///< INCORRECT
    adventure_books,                            ///< INCORRECT
    storyBooks                                  ///< INCORRECT
};
```

### Naming Global Constant Values and Macros

-   Constant literals can be used with each one "UpperCamelCase" , "UPPERCASE" and Macro Case styles.
-   Macros using with both "UPPERCASE" and "MACRO_CASE" styles.

```cpp
const int MYGLOBALVAR = 0;                      ///< OK
const double PI = 3.14;                         ///< OK

const int MyCharacterHealth                     ///< OK
const int monsterHealth                         ///< INCORRECT
```

```cpp
#define MYEXAMPLE                               ///< OK

#define MyExample                               ///< INCORRECT
```

## Comments

Multi Line Comments :

```cpp
/**
 *  @brief comment will come here...
 *
 *  comment will come here...
 *  comment will come here...
**/
```

Single Line Comments :

```cpp
///< This is single line comment.
///< This is another single line comment.
```

> This style guide using doxygen type comment.

### Funcitons/Methods

```cpp
class Foo
{
    public: int void boo() 
    {
        ///< Code ...
    }
};

```

### Parameters

```cpp

```

### Returns

```cpp

```

### Class

```cpp

```

### Namespace

```cpp

```

### Enum

```cpp

```

### Template Parameters

```cpp

```

### Throw & Exceptions

```cpp

```

### Notes

```cpp

```

### Overload

```cpp

```

### See Also

```cpp

```

### Bug

```cpp

```

### Todo

```cpp

```

```cpp
/**
 *  @brief
 *  this explain will come here..
 *
 *  @param
 *  this explain will come here..
 *
 *  @return
 *  this explain will come here..
 *
 *  @class
 *  this explain will come here..
 *  
 *  @todo
 *  this explain will come here..
 *
 *  @namespace
 *  this explain will come here..
 *  
 *  @enum
 *  this explain will come here..
 *
 *  @bug
 *  this explain will come here..
 *
 *  @tparam
 *  this explain will come here..
 *
 *  @throw
 *  this explain will come here..
 *  
**/
```
>>>>>>> Stashed changes
