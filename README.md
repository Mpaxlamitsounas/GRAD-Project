# GRAD Project

A set of software and specifications for a CPU (GRAD Machine), a programming language (GRAD Language), and a compiler and assembler (GRAD Compiler).

The architecture and ISA of the CPU are based on the book "[The Elements of Computing Systems](https://www.nand2tetris.org/)" by Noam Nisan and Shimon Schocken, which has been adapted into the "nand2tetris" course.
The GRAD Machine itself is an expansion and implementation of that architecture in the "[Digital](https://github.com/hneemann/Digital)" circuit simulator, providing a different approach to the traditional HDL implementation the book and course task the reader with creating.

The syntax of the language is similarly based on the book, although it diverged much earlier compared to the GMachine.
Many language features have been designed with ease-of-use in mind, making the process of writing in GLang less tedious and error prone.

The GRAD Compiler parses, assembles, and compiles GLang source code files into GMachine instruction code. The compiler as a whole is entirely original. \
Errors encountered while processing a file do not halt the process and are instead queued to be logged, this approach allows for more than one error to be caught per run. \
Most of the shorthands introduced in the GLang result in lines of code that are equivalent to multiple instructions, "decompressing" these into elemental instructions is done by the GCompiler.
This process might introduce inefficiencies which the compiler solves by applying optimisations during and after decompression.

Get the project with `git clone --recursive https://github.com/Mpaxlamitsounas/GRAD-Project`. \
The GCompiler requires Python3.12 or newer. \
Read the documentation for many, many more details.
