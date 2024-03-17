***

```SHELL
$ gcc -Wall -I/opt/gdbm-1.8.3/include dbmain.c -lgdbm
```

 ‘-I’ allows the program to be compiled, but not linked.

```SHELL
$ gcc -Wall -I/opt/gdbm-1.8.3/include -L/opt/gdbm-1.8.3/lib dbmain.c -lgdbm
```

The following command line allows the program to be compiled and linked.

Additional directories can be added to the include path using the envi-
ronment variable C_INCLUDE_PATH (for C header files) or CPLUS_INCLUDE_
PATH (for C++ header files).

```C
C_INCLUDE_PATH=/opt/gdbm-1.8.3/include
export C_INCLUDE_PATH
```

With the environment variable settings given above the program ‘dbmain.c’ can be compiled without the ‘-I’ and ‘-L’ options.

```SHELL
$ gcc -Wall dbmain.c -lgdbm
```

