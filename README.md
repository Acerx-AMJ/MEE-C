# MEE
Mathematical expression evaluator - a CLI calculator. This works very similarly to an interpreted programming language but does not include any statements. All functions can be seen in [include/functions.hpp](include/functions.hpp) and all constants can be seen in [include/lexer.hpp](include/lexer.hpp). Very similar to the [C++ counterpart](https://github.com/Acerx-AMJ/MEE) but has less readable errors and constants are handled at parse-time.

## Features:
- Constants: pi, e, phi, gamma and tau
- Functions: sin, cos, tan, sqrt, log, randf, randi and many more
- Operators: +, -, /, *, ^ (exponentiation), ! (factorial), % (percent) and ()

## How it works:
User Input --> Lexer --> Parser --> Evaluator --> Result

1. Program retrieves input from the user.
2. Lexer turns characters into words (tokens)
3. Parser reads the tokens and produces the AST tree
4. Evaluator evaluates the AST tree and produces the final result

## Building
This project is made in C and can be built using CMake:
```bash
cmake -B build
cmake --build build
```
The executable will be located in `build/mee`. Or build using your favorite compiler:
```bash
gcc -Iinclude src/*.c -o mee -lm # remove -lm on Windows
```

## Credits
This project was made by Daniel Vishnevsky and is licensed under MIT License. It was made in March of 2025 and published on October 2026 as an effort to make all of my projects open-source.
