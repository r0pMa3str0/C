***
```SHELL
$ gcc -Wall hello.c -o hello
```

The option ‘-Wall’ turns on all the most commonly-used compiler warnings—it is recommended that you always use this option.

```SHELL
$ gcc -Wall main.c hello_fn.c -o newhello
```

To compile these source files with gcc.

***
## Compiling files independently

Creating object files from source files.

```SHELL
$ gcc -Wall -c main.c
$ gcc -Wall -c hello_fn.c
```

Creating executables from object files

```SHELL
gcc main.o hello_fn.o -o hello
```

This is one of the few occasions where there is no need to use the ‘-Wall’
warning option, since the individual source files have already been success-
fully compiled to object code. 


```SHELL
$ gcc -Wall calc.c /usr/lib/libm.a -o calc
```

Linking with external libraries.

```SHELL
$ gcc -Wall calc.c -lm -o calc
```

To avoid the need to specify long paths on the command line, the
compiler provides a short-cut option ‘-l’ for linking against libraries. For
example, the following command.

```SHELL
$ gcc -Wall data.c -lglpk -lm
```

For example, a program ‘data.c’ using the GNU Linear Programming library ‘libglpk.a’, which in turn uses the math library ‘libm.a’, should be compiled as.




