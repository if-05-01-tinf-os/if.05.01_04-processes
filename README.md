### if.05.01 TINF Operting Systems

# Assignment 4: Processes
## Objective
The goal of this week's assignment is to make you familiar with processes in C and in Java.

## Required Tasks
Write the following program

### Simple Shell
You are to implement a simple shell (command interpreter) that behaves similarly (but not identically) to the UNIX shell. When you type in a command (in response to its prompt), it will create a thread that will execute the command you entered. Multiple commands can be entered on a single line, separated by '&' (ampersand) characters. Your shell will run them all concurrently and prompt for more user input when they have all finished.

You do not need to implement pipes or re-direction of standard input and standard output, and & at the end of a command has no special meaning (it does not mean to run the command in the "background"). You must be able to handle an arbitrary number of commands per line -- each with an arbitrary number of arguments separated by arbitrary amounts of white space (blanks or tabs). Your program should recover gracefully from such errors as unknown commands by printing an error message and continuing.

- Implement this shell in C
- Implement this shell in Java

### Hints
- Splitting a string along a character in C can be done by using the function `strtok`
- Getting the output from a process started in Java can be done via a `BufferedReader`. The Reader is constructed with a `StreamReader` which itself takes the `InputStream` of the process to be investigated. This results in the line

```java
BufferedReader input = new BufferedReader(new InputStreamReader(p.getInputStream()));
```

- Divide the assignment in smaller steps
   - Try to create and run a process which is hard coded in your program
   - Play around with `strtok` to get a feeling for the behavior of this function
   - ...