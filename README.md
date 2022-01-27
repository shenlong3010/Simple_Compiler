# Simple_Compiler
Inspired by Brian Robert Callahan in https://briancallahan.net/blog/20210814.html

Note: This is just good enough compiler, not state-of-the-art clang or gcc compiler. This is just for learning purpose.\n

Developed on: tux - Unix server built from Drexel.

A language to compile: PL/o (https://en.wikipedia.org/wiki/PL/0)

A language to implement PL/o compiler: C

Development environment: unix

IDE: vim

There are 3 main parts for this compiler: the lexer, the parser, and the code generator. The lexer's job is to take the free-form source code and turn it into a series of tokens, the individual units of the language. The parser's job is to take that series of tokens and ensure that their ordering follows the rules of the language syntax. The code generator's job is to produce equivalent C language.
