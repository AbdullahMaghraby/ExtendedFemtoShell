# ExtendedFemtoShell
Shell that echo entered strings and have multiple internal commands

##Program Architecture

###Developing code as modules in seperate files 
1- default mode if string entered is not command shell will echo it
2- if enter rand will print random number
3-fact will take a number then print its factorial
4-fib will take number then print its fibonacci series
5- exit for programm quit

##Developing Stages
###Developing ordinary modules in separate files
main.c contains main function at this stages
###compiling files

    ```` bash
    $ gcc -c *.c
    $ gcc *.o -o myExtFemtoShell
    $ ./myExtFemtoShell
       ````
###first stage test
![](/1.png "1st stage test")

###Static Library Creation

    ```` bash
    $ gcc -c rand.c fact.c fib.c
    $ ar -rs libFemtoShell.a rand.o fact.o fib.o
    $ gcc -c prog.c
    $ ggcc -o myFemtoShellStLib prog.o ./libFemtoShell.a
    ````
    
###Testing Static Lib stage
![](/2.png "2nd stage test")

###Dynamic Library Creation

    ```` bash
    $ gcc -shared -fpic -o libvector.so addvec.c multvec.c
    $ gcc -o myDyFemtoShell dyProg.c ./libFemtoShell.so
    ````
 ###Testig Dynamic Lib
 ![](/3.png "3rd stage test")
 
 ###Comparing 2 Libraries exes sizes
 ![](/4.png "Comparing Libraries sizes")
 
