###A CONCISE INTRODUCTION TO VARIADIC FUNCTIONS IN C

#Why use variadic functions?
Whenever we are writing new functions in most cases,
our function parameters are usually known to us already.
But what happens in a case whereby we do not know the number of arguments
our function will take. This is where variadic functions are useful.

#What are variadic functions?
Variadic functions are simply functions that can take a variable number of arguments.
This is a powerful tool for creating flexible and interesting functions.
An existing example is the printf function.

#How to declare/recognize a variadic function - Syntax:
Variadic functions can easily be spotted by the elipses(...) at the end of the function argument.

Syntax: type function_name(type variable_name, ...);

##Understanding the Syntax:
* type - implies data type (int, void etc)
* function_name - name you'd love to call your function
* function arguments i.e (type variable_name, ...) - Notes about function args:
	* There are two types of arguments in a variadic function
		1. Fixed argument (Must be defined at function declaration - eg variable_name in the syntax above)
		2. Variable arguments (denoted by the ... symbol - not known at function declaration)
	* Variadic functions take at least one (1) fixed argument.

##Accessing variadic functions:
To work with variadic functions, #include <stdarg.h>
This header file contains the methods used to manipulate variadic function arguments.
We will understand the use for each method better in the later part of this article.

#The following methods are available within the stdarg.h file:
* va_list: Is a pointer to the variable functions (PS: it behaves like a data type)
* va_start: Begins processing the function arguments. It takes two arguments in itself)
	* va_list
	* argN - the last fixed argument in the variadic function)
  Thus: va_start (va_list, argN);
* va_arg: Used to access the variable arguments (...) and perform operations on them.
	It takes two arguments: va_arg(va_list, type);
	PS: type defines the data type to be expected/supplied when calling that argument.
* va_end: Stops traversing the variadic function arguments. It takes va_list as argument.
	i.e va_end(va_list);
* va_copy: makes a copy of the variadic function arguments. It takes two arguments.
	va_copy(va_list destination, va_list source);

##Work example:
We will use two simple examples to illustrate the workings of the variadic function.
1. A function that adds numbers.
2. A function the prints a digit when passed 'd' or float when passed 'f'.

#include <stdarg.h>
#include <stdio.h>

 void print(char format[5], ...)
 {
        va_list val;
 
        va_start(val, format);

        for (int i = 0; i < 5; i++)
        {
                if (format[i] == 'd')
                {
                        int a = va_arg(val, int);
                        printf("%d ", a);
                }
                else if (format[i] == 'f')
                {
                        double b = va_arg(val, double);
                        printf("%.2f ", b);
                }
                else if (format[i] == 'n')
                        putchar('\n');
        }
        va_end(val);
 }
