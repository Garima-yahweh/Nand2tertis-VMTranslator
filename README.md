# Nand2Tetris VM Translator

## 📌 Overview

This project is a **complete VM Translator** for the **Nand2Tetris** course, implemented entirely in **a single C++ source file**. It translates **Virtual Machine (VM) commands** into **Hack assembly language**, enabling VM programs to run on the Hack computer.

The translator supports **arithmetic/logical operations**, **memory access**, **program flow**, and **function call/return semantics**. It can process **a single `.vm` file or a directory containing multiple `.vm` files** and generates a single `.asm` output.

---

## 🚀 Features

* Full VM-to-Hack assembly translation
* Arithmetic & logical commands: `add`, `sub`, `neg`, `eq`, `gt`, `lt`, `and`, `or`, `not`
* Memory access commands: `push`, `pop`

  * Supported segments: `constant`, `local`, `argument`, `this`, `that`, `temp`, `pointer`, `static`
* Program flow commands: `label`, `goto`, `if-goto`
* Function commands: `function`, `call`, `return`
* **Bootstrap code** support (`SP=256`, calls `Sys.init`) when translating directories
* Static variables scoped per VM file
* Single-file C++ implementation (parser + code writer in one `.cpp`)

---

## 🛠️ Technologies Used

* **Language:** C++ (uses C++17 filesystem)
* **Concepts:** Stack-based Virtual Machine, Assembly Code Generation, Compiler Design Basics

---

## 📂 Project Structure

```
VMTranslator/
├── VMTranslator.cpp   // Contains main logic, parser, and code writer
├── tests/             // VM test files (if any)
└── README.md
```

---

## ▶️ How to Run

### Compile

```bash
g++ -std=c++17 VMTranslator.cpp -o VMTranslator
```

### Execute

Translate a single VM file:

```bash
./VMTranslator SimpleAdd.vm
```

Translate a directory containing multiple VM files:

```bash
./VMTranslator MemoryAccess/
```

* For a single file, output will be `FileName.asm`
* For a directory, output will be `DirectoryName.asm`

---

## 📘 Learning Outcomes

* Clear understanding of **VM command parsing and translation**
* Hands-on experience with **stack-based execution models**
* Practical implementation of **function call frames and control flow**
* Improved proficiency in **C++ systems programming**

---

## 📖 References

* [Nand2Tetris Course](https://www.nand2tetris.org/)
* *The Elements of Computing Systems* by Noam Nisan and Shimon Schocken

---

## 🧑‍💻 Author

**Badugu Garima**
C++ | Systems Programming | Computer Science Student

---

## 📄 License

This project is created for **educational purposes** as part of the Nand2Tetris course.
can you make this lake a text not like Ai generated canva
