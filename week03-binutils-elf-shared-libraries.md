
This week, we are testing shared libraries in action. Additionally, we are examining the structure of executable files in Linux, including the various sections and their purposes. We are also reviewing the tools included in the binutils package to work with our files. 

#### Linux executable files
- In Linux, executable files are typically in the ELF (Executable and Linkable Format) format. Think of ELF as a container that holds all the bits and pieces needed to run your program.
- ELF files contain several key parts:
	- A header with basic info about the file
	- Sections that hold actual program code and data
	- Segment info that tells the system how to load the file
- Some important sections you'll find in an ELF file:
	- .text: This is where your actual machine code lives
	- .data: Contains initialized global variables
	- .bss: Holds uninitialized global variables
	- .rodata: Stores read-only data like string constants


#### Exploration Task
 Using an AI assistant (such as ChatGPT or Claude) get understanding of the following questions/concepts:
- What the main difference between executable and object files
- What the difference between static and dynamic linking in Linux
- Why ELF contain sections
- Could or not executable file be loaded to memory as is
- Why executable file which is built on for one operating system, could not be launched in another
- Is any way to make an executable file working in different operating systems
 
---
#### Practice with binutils

!IMPORTANT: read assignment to the end before doing it.

Make a hello world program, compile it (you can use any task solution from previous week) and answer the following questions (getting answers with help one of the tools from binutils package):
- list all ELF sections from executable
- list all names included in your executable, corresponded to program code
- provide size in bytes for 'text', 'data', and 'bss' sections
- provide difference in executable file size before and after removing all symbols
- provide all dynamic libraries linked to your executable

For each task you have to provide, not only answer, but also command (or commands) you run to get the answer. See exploration directory in template repo

#### Shared library with command line input
You need to write a program that the user runs with a single **command-line argument** containing a number. 

The program must be linked with the library containing the 'process' function, which processes the input number.
```
int process(int number);
```
You need to create two versions of libraries containing the 'process' function, each placed in a separate library(shared object). Depending on the environment in which the executable is run, one version of the function will be used or the another. Let us say that the first version should multiply number to 10 and second version divides by 2.

Investigate, how to use LD_LIBRARY_PATH environmental variable to control where dynamic linker searching shared objects. 

Edit 'Makefile' in your repo to support both application launch variants.

All solutions should be send via github according the github-classroom link provided by teacher. (If you are not familiar with github yet, please keep all files. You will be able to submit them after lecture on git)

#### What would help
- ChatGPT, search engines like google, bing, etc
- People in Discord channel #pr2024
- man ld.so

#### Stuck with something?
- Ask a question in the class chat, everybody welcome to answer and help
- Tag @krinkin in course chat if the problem too unclear how to approach

#### Want to contribute of found a bug?
- Feel free to clone [the repo](https://github.com/programming-fundamentals-class/supplementary-2024), send a pull request

## Pre-reading for the next week

#### Mandatory
- Brian W. Kernighan and Dennis M. Ritchie, The C programming Language Prentice-Hall in 1988
	- Chapter 4: Functions and Program Structure
- 
#### Optional
- TBD
 