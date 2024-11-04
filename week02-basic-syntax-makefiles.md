
This week, we are learning to write simple programs in the C language and to use basic syntax. Additionally, we are examining how to create and utilize dynamic libraries in C. Starting this week, we start using AI assistants such as ChatGPT (does not required registration), Claude or others

#### Concepts self exploration with AI-assistants
Today you have to explore the following concepts: Makefiles and shared objects (dynamic linked libraries)

Usually the first step, initiating working with AI assistant is the proper context prompt. For current class it could be like
```
I am the first semester university student who need to study C programming language in Linux environment (using only terminal-based tools). Currently I am focusing on the following concepts: Basic C syntax, Makefiles, shared objects. I will ask questions one by one about those concepts. You need to provide me very precise information with corresponding references to linux man pages. 
```

LLM-based assistants usually have limited context window -- it is a memory where the current dialog and corresponding files are stored. It means, that it is better to have separate conversation at least for different topics (we have 2 topics for the class). Also it is useful to restart chat if you want to study another aspect of the same concept.

#### Explorations Task
 Using an AI assistant (such as ChatGPT or Claude), explore the concepts of **makefiles** and **shared objects (dynamic libraries)** in Linux. 
 
 Follow these steps to guide your learning:

1. Makefiles: a) Ask the AI to explain what a makefile is and its purpose in software development. b) Request an example of a simple makefile for a C project with multiple source files. c) Ask the AI to explain each line of the example makefile. d) Inquire about common makefile rules like 'all', 'clean', and how to use variables in makefiles. e) Ask LLM how to find corresponding information in Linux man pages system.

2. Dynamic Libraries: a) Ask the AI to explain what dynamic libraries are and their advantages in Linux. b) Request step-by-step instructions on how to create a simple dynamic library in C. c) Ask for an example of how to link and use a dynamic library in a C program. d) Inquire about the difference between static and dynamic libraries.
  
3. Integration: a) Ask the AI how to modify a makefile to compile and link a program with a dynamic library. b) Request an explanation of the LD_LIBRARY_PATH environment variable and its role in using dynamic libraries.
   
4. Practice: a) Based on the information provided by the AI, try to write your own makefile for a simple C project. b) Attempt to create a basic dynamic library and use it in a C program. c) If you encounter any issues, ask the AI for help in debugging or clarifying concepts.
   
5. Reflection: a) Summarize what you've learned about makefiles and dynamic libraries. b) Identify any areas where you need further clarification or practice.

Remember to critically evaluate the AI's responses and cross-reference with man pages or other reliable sources. If you're unsure about any information provided, feel free to ask for clarification or additional examples. If you stuck with understanding or feel lost, ask your human instructor for help.

---
#### Practice C syntax

Depending on your basic experience and previous reading you need to solve at least 10 tasks provided below. 

All solutions should be send via github according the github-classroom link provided by teacher. (If you are not familiar with github yet, please keep all files. You will be able to submit them after lecture on git)

Whole assignment solution should have the following file structure
```
├── concepts                 -- folder where you put chats with llm
│   ├── makefiles              -- particular dialogs, you can have many
│   └── shared-oblects           | files here 
├── task01                   -- folder with solution of the first task
│   ├── Makefile               -- makefile
│   └── solution.c             -- source code 
├── task010
│   ├── Makefile             | you can have more source files
│   └── solution.c

```

Note: one of the task should mandatory built as a two separated binaries -- executable and library
##### Simple Tasks

1. Write a program that outputs the string "HELLO WORLD!" to the console.
2. Write a program that takes a NAME as input from the console and outputs the string "HELLO, NAME!" to the console.
3. Fill a list of 15 integers with values entered from the keyboard and output these values to the console in reverse order.
4. Find and output the sum of 15 integers (numbers must be entered from the console).
5. Find and output the first negative even number from 15 entered integers.
6. Find and output the last negative odd number from 15 entered integers.
7. Find and output the arithmetic mean of 15 entered integers.
8. The program receives a string of numbers separated by semicolons as input. Find the product of these numbers.
9. The program receives a string of Latin alphabet characters separated by semicolons as input. Find the number of these strings.
10. Count and output the number of spaces and exclamation marks in 15 entered characters.
11. Output the indices of spaces in 15 entered characters. If there were no spaces in the characters, output the "-" symbol.
12. The program receives one of three symbols as input: -, +, \*, and two integers. Output the result of the operation for the first and second number. (For example, if the input is '-', 30, 10, the program should output 20.)
13. The program first receives a number n as input, and then n integers. Determine if the numbers are ordered in non-decreasing order. Output "Yes" or "No". Save the numbers for processing in a list.
14. The program receives a string as input, representing a single word of Latin letters. Determine if the word is a palindrome (reads the same in both directions, e.g., "anna"). Output "Yes" or "No".
15. Fill a two-dimensional list with zeros and output it to the console:
    1. Size 10×10
    2. Size 5×10
    3. Size 10×5

#### Hard Tasks
16. The program receives a number n, x as input, followed by n integers that are the coefficients of a polynomial of degree n. The coefficients are given in descending order of degrees. Calculate and output the value of the polynomial at point x. 

	 *Int the following tasks assume that the program first receives the number of elements N≤100 as input, followed by N numbers. *

17. Find the difference between the maximum and minimum number in this list. 
18. Find the sum of the list elements located before the minimum element. 
19. Find the sum of the list elements located after the last element equal to zero. 
20. Find the sum of the absolute values of the list elements located after the element with the maximum absolute value. 
21. Find the sum of the absolute values of the list elements located after the first element equal to zero. 
22. Find the product of the list elements located between the first and second zero elements. 
23. Find the sum of the list elements located between the first and last negative elements. 
24. Find the product of the list elements located between the maximum absolute value and minimum absolute value elements. 

#### What would help
- ChatGPT, search engines like google, bing, etc
- People in Discord channel #pr2024
- [Linux Bash Shell Cheat Sheet](https://oit.ua.edu/wp-content/uploads/2020/12/Linux_bash_cheat_sheet-1.pdf)
- [Vim cheat sheet](https://web.stanford.edu/class/cs110/summer-2021/handouts/vim-cheat-sheet/)
- [Tmux Cheat Sheet & Quick Reference](https://tmuxcheatsheet.com/)

#### Stuck with something?
- Ask a question in the class chat, everybody welcome to answer and help
- Tag @krinkin in course chat if the problem too unclear how to approach

#### Want to contribute of found a bug?
- Feel free to clone [the repo](https://github.com/programming-fundamentals-class/supplementary-2024), send a pull request

## Pre-reading for the next week

#### Mandatory
- Brian W. Kernighan and Dennis M. Ritchie, The C programming Language Prentice-Hall in 1988
	- Chapter 2: Types, Operators and Expressions
	- Chapter 3: Control Flow
- Explore the following concepts with 'man' and ChatGPT
	- 'make' (command line utility to build programms)
	- 'binutils'
	  
	*!! Keep chats with AI-assistant, they should be pushed to git later*

#### Optional
- [Understanding the Origins and the Evolution of Vi & Vim](https://pikuma.com/blog/origins-of-vim-text-editor)
- [The TTY demystified](https://www.linusakesson.net/programming/tty/)
 