# Expression Evaluator for Rationals

A C++ based expression evaluator that supports arithmetic operations on **unlimited-precision integers and rational numbers**.

The project implements custom integer and rational number classes along with expression parsing, expression trees, symbol tables, and evaluation logic.

---

## 📌 Project Overview

The main goal of this project is to evaluate mathematical expressions involving integers and rational numbers without relying on standard fixed-size integer limitations.

The project includes implementations for:

- Unlimited-precision integers
- Unlimited-precision rational numbers
- Expression parsing
- Expression trees
- Symbol tables
- Arithmetic evaluation
- Test cases

### Overall Flow

```
Input Expression → Parser → Expression Tree → Evaluator → Symbol Table → Rational/Integer Operations → Result
```

---

## 🛠️ Technologies Used

- C++ / C++11
- Object-Oriented Programming
- Expression Trees
- Symbol Tables
- Arbitrary/Unlimited Precision Arithmetic
- File Handling
- Makefile

---

## 📂 Project Structure

```
expression-evaluator-for-rationals/
├── Makefile
├── metadata.yml
├── drivercode.cpp
├── entry.cpp / .h
├── evaluator.cpp / .h
├── exprtreenode.cpp / .h
├── symtable.cpp / .h
├── ulimitedint.cpp / .h
├── ulimitedrational.cpp / .h
├── breath.cpp
├── a.cpp
└── test_cases/
```

---

## 🔍 Main Components

**1. UlimitedInt** (`ulimitedint.cpp/.h`)
Implements integers that go beyond the limits of standard C++ integer types. Serves as the foundation for handling large integer values.

**2. UlimitedRational** (`ulimitedrational.cpp/.h`)
Represents rational numbers (numerator/denominator) using the unlimited-precision integer implementation — e.g. `3/4`, `10/7`, `-5/8`. Enables arithmetic without fixed-size integer limits.

**3. Expression Tree** (`exprtreenode.cpp/.h`)
Represents expressions as trees so operators and operands can be processed in a structured manner.

Example — `a + b`:
```
   +
  / \
 a   b
```

**4. Evaluator** (`evaluator.cpp/.h`)
Processes the expression tree and calculates the result, working with the integer/rational classes.

**5. Symbol Table** (`symtable.cpp/.h`)
Stores and maintains variables and their associated values while evaluating expressions.

**6. Entry** (`entry.cpp/.h`)
Represents individual entries maintained by the evaluator and symbol table.

---

## 🏗️ Architecture

```
                   ┌──────────────────┐
                   │   Input / Driver │
                   └────────┬─────────┘
                            ▼
                   ┌──────────────────┐
                   │      Parser      │
                   └────────┬─────────┘
                            ▼
                   ┌──────────────────┐
                   │ Expression Tree  │
                   └────────┬─────────┘
                            ▼
                   ┌──────────────────┐
                   │     Evaluator    │
                   └───────┬───┬──────┘
                           │   │
              ┌────────────┘   └────────────┐
              ▼                             ▼
      ┌───────────────┐             ┌──────────────┐
      │  Symbol Table │             │    Rational  │
      └───────────────┘             └──────┬───────┘
                                            ▼
                                  ┌──────────────────┐
                                  │  Unlimited Int   │
                                  └──────────────────┘
```

---

## 🧮 Example

Expression: `3/4 + 5/6`

```
    +
   / \
 3/4  5/6
```

The rational arithmetic implementation calculates the resulting rational value.

---

## 🧪 Test Cases

The `test_cases/` directory contains test inputs used to verify the evaluator's behavior.

---

## 💡 Key Features

- Custom unlimited-precision integer implementation
- Custom rational number implementation
- Expression tree based evaluation
- Symbol table support
- Modular C++ implementation
- Makefile based compilation
- Dedicated test cases

---

## 🚀 How to Run

**Prerequisites:** a C++ compiler and `make`. Check with:
```bash
g++ --version
make --version
```

**1. Clone the repository**
```bash
git clone https://github.com/Abhinav4565/expression-evaluator-for-rationals.git
cd expression-evaluator-for-rationals
```

**2. Build the project**
```bash
make
```

**3. Run the program**
```bash
./evaluator
```
(The exact executable name depends on the target defined in the Makefile — check with `ls`.)

---

## 📁 Source Files

| File | Purpose |
|------|---------|
| `drivercode.cpp` | Driver program |
| `entry.cpp` / `entry.h` | Entry implementation / declarations |
| `evaluator.cpp` / `evaluator.h` | Expression evaluation implementation / declarations |
| `exprtreenode.cpp` / `exprtreenode.h` | Expression tree implementation / declarations |
| `symtable.cpp` / `symtable.h` | Symbol table implementation / declarations |
| `ulimitedint.cpp` / `ulimitedint.h` | Unlimited integer implementation / declarations |
| `ulimitedrational.cpp` / `ulimitedrational.h` | Unlimited rational implementation / declarations |
| `Makefile` | Build configuration |
| `metadata.yml` | Project metadata |

---

## 🔧 Development

Rebuild after changes:
```bash
make
```

Clean build files (if a `clean` target exists):
```bash
make clean
```

---

## 🐛 Troubleshooting

**`g++: command not found`**
Install a C++ compiler / Xcode Command Line Tools on macOS:
```bash
xcode-select --install
g++ --version
```

**Permission denied when running the executable**
```bash
chmod +x <executable-name>
./<executable-name>
```

**Check available Makefile targets**
```bash
cat Makefile
```

---

## 📈 Future Improvements

- Better expression parsing
- More arithmetic operators
- Improved error handling
- More extensive test coverage
- Additional rational-number operations
- Improved input validation
- Better documentation
- Cross-platform build support

---

## 👨‍💻 Author

**Abhinav Yadav**
GitHub: [https://github.com/Abhinav4565](https://github.com/Abhinav4565)

## 📄 License

This project is developed for educational and learning purposes.
