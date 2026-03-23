## Stream editor

A non-interactive text editor for performing basic text transformations on an input stream, such as a file or input from a pipeline. It processes text line by line and applies the editing commands you specify.

It can:

![[sed commands image.png]]

`sed` works with two workspaces: The pattern space holding the line being modified, and the hold space which can temporarily store a line for later use.

### Syntax

```bash
sed [OPTIONS] 'COMMAND' [INPUTFILE...]
```

Where:
- OPTIONS: Optional flags for modifying behaviour
- COMMAND: The command/sequence of commands to execute on the input file
- INPUTFILE: One or more input files to be processed

### Common Flags

- [[-i (sed)]]
- [[-n (sed)]]
- [[-e (sed)]]
- [[-f (sed)]]
- [[-r (sed)]]

### Examples

Consider the text file as input:

```bash
cat > file.txt
```

```txt
unix is great os. unix is opensource. unix is free os.  
learn operating system.  
unix linux which one you choose.  
unix is easy to learn.unix is a multiuser os.Learn unix .unix is a powerful.
```

#### 1. Sample Commands

Replacing/substituting string: `sed` is mostly used to replace the text in a file. For example, replacing "unix" with "Linux" in the file:

```bash
sed 's/unix/linux/' file.txt
```

Output:

```txt
linux is great os. unix is opensource. unix is free os.  
learn operating system.  
linux linux which one you choose.  
linux is easy to learn.unix is a multiuser os.Learn unix .unix is a powerful.
```

Here:
- The "s" is the substitution operation.
- The "/" are delimiters
- "unix" is the search pattern
- "linux" is the replacement string

By default, this command replaces only the first occurrence of the pattern in each line and not the second, or third, etc. 

## 2. Replacing the nth Occurrence of a Pattern 

We can use the following syntax:

```bash
sed 's/old_word/new_word/n' filename
```


