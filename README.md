Nand2Tetris VM Translator
Overview

This project is a VM Translator built as part of the Nand2Tetris course. The program converts Virtual Machine (VM) code into Hack assembly language so that VM programs can run on the Hack computer.

The entire translator is written in a single C++ file and supports translating both a single .vm file and a directory containing multiple VM files into one .asm output file.

Features

Translates VM code into Hack assembly

Supports arithmetic and logical commands
(add, sub, neg, eq, gt, lt, and, or, not)

Supports memory access commands
(push, pop)

Handles all required memory segments:
constant, local, argument, this, that, temp, pointer, static

Supports program flow commands
(label, goto, if-goto)

Implements function commands
(function, call, return)

Generates bootstrap code (SP = 256) and calls Sys.init when a directory is given as input

Static variables are handled separately for each VM file

Technologies Used

Language: C++ (C++17 standard)

Key Concepts:
Stack-based virtual machines, assembly code generation, function call handling

Project Structure
VMTranslator/
├── VMTranslator.cpp   // Main file containing parser and code writer
├── tests/             // VM test files (optional)
└── README.md

How to Run
Compile
g++ -std=c++17 VMTranslator.cpp -o VMTranslator

Run

For a single VM file:

./VMTranslator SimpleAdd.vm


For a directory containing multiple VM files:

./VMTranslator MemoryAccess/


Single file input → FileName.asm

Directory input → DirectoryName.asm

What I Learned

How a stack-based virtual machine works

How VM commands are translated into low-level assembly instructions

How function calls, returns, and stack frames are implemented

Improved understanding of C++ and file handling

References

Nand2Tetris official course material

The Elements of Computing Systems — Noam Nisan & Shimon Schocken

Author

Badugu Garima
Computer Science Student | C++ Programming

License

This project was developed for educational purposes as part of the Nand2Tetris course.
