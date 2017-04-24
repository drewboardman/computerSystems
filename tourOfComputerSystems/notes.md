A Tour of Computer Systems
=========================

  - the ASCII standard represents characters with an integer value of size == 1 byte (8 bits)
  - text files consist exclusively of ASCII characters. *All* other files are known as binary files.
  - a program like `hello_world.c` is a high level abstraction to be read by humans
    - it must be translated into machine-language instructions in order to be run
    - these are known as *executable object programs/files*

### Steps for compilation
  - When you run something like `gcc -o hello hello.c`, there are 4 intermediary steps

#### 1. Preprocessing Phase(`cpp`)
  - this takes the header files (like `stdio.h`) and inserts the contents of it directly into the the program. The result is usually `hello.i`

#### 2. Compilation Phase(`cc1`)
  - this translates the `.i` text file into another text file `hello.s` that contains assembly language

#### 3. Assembly Phase(`as`)
  - this takes the assembly language and translates it into machine language instructions
  - the result is called a *relocatable object program*
  - stored in `hello.o`
  - contents are binary

#### 4. Linkage Phase(`ld`)
  - this takes other `.o` object programs and links their functions into our program
  - `printf` for instance would exist in `printf.o`
