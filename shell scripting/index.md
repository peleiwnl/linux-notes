Users communicate with the OS through a shell, which interprets and executes commands entered in the terminal.

Shell scripting allows users to combine multiple commands into a single file and execute them as a program, enabling structured task automation and system control:
- Forms the foundation of CLI interaction in Linux systems
- Enables automation of repetitive tasks
- Supports batch execution of multiple commmands
- Widely used in DevOps

## Common Shell Programs in Linux

- Bash - Most widely used
- Csh
- Ksh

## Shell Scripts

A shell script is a text file containing a series of commands that the shell can interpret and execute, typically having a .sh extension, such as:

```
myscript.sh
```

### Uses and advantages of Shell Scripts

1. Automate Repetitive Tasks - Such as clean-up, backups, server updates
2. Reliable and Consistent - Run every time without mistakes, removing human error
3. Native Support on Linux Systems - no additional installations
4. Great for linking commands to work together - Pass the output of one command into another etc
5. Ideal for IT, DevOps and Monitoring
6. Lightweight and easy to write

### Syntax

#### Shebang (#!):
- First line in a shell script typicall starts with `#!/bin/bash`
- Specifies which shell should interpret the script

#### Comments:
- Lines starting with # are comments and ignored during execution
- Useful for documenting the script

#### Commands:
- Shell commands like ls, cd, echo, pwd are executed sequentially

#### Variables:
- Used to store values or user input for reuse in commands
- Example: `MRDIR="/home/user/projects`

#### Control Structures:
- Conditional statements: if...then...else, case
- Loops: for, while, until

#### Functions:
- Reusable blocks of code that can be called multiple times within a script

### Example Script:

```
#!bin/bash
# This script displays the current directory and lists all files

echo "Current Directory: "
pwd

echo "Files in Directory:"
ls -l

```

![[bash scripting base example.png]]



#shellscripting