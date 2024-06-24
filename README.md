# Lexer and Parser forr mini C Language

### Lax and Yacc are used for lexical analysis and parsing, respectively.             

#### Lax (Lexical Analyzer) , is a lexical analyzer that breaks up an input stream into more usable elements, such as tokens. Its main job is to identify the “interesting bits” in a text file. For example, in a compiler for the C programming language, the symbols {}, (), and ; have significance on their own, while the letter a usually appears as part of a keyword or variable name.

#### Yacc (Yet Another Compiler-Compiler) , is a parser generator that takes as input a specification of a syntax and produces as output a procedure for recognizing that language. It is a program that handles the input process and can be used to create a parser for a specific language. Yacc is often used to give structure to the tokens produced by Lax. 

Lax can be used to create a compiler for a programming language, breaking up the input stream into tokens such as keywords, identifiers, and symbols.Yacc can be used to create a parser for a specific language, analyzing the structure of the input stream and recognizing the language’s syntax.

### Lexer Details:

Recognizes tokens such as arithmetic operators, comparison operators, data types, keywords, etc.
Ignores whitespace, comments, and unrecognized characters.
Provides actions like printing token information and storing values.
Uses yywrap function to indicate end of input.

### Yacc File Details:

Includes headers like <stdio.h> and <stdlib.h>.
Defines external functions like yyerror and variables like yyin.
Uses union for holding string or integer values.
Defines tokens, start symbol, grammar rules, and main function.

### Grammar Rules:

Includes rules for program structure, variable declarations, functions, statements, expressions, etc.
Supports int and char data types.
Handles compound statements, assignments, function calls, and more.

### Main Function:

Handles program startup, file I/O, and parsing.
Opens input, lexer output, and parser output files.
Calls yyparse() for parsing and closes files afterward.
Overall Functionality:

This C program serves as a parser for a mini-C language.
Interacts with a lexer to obtain tokens and uses Yacc for defining grammar rules.
Analyzes token stream to verify adherence to defined grammar.
