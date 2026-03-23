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

#### 2. Replacing the nth Occurrence of a Pattern 

We can use the following syntax:

```bash
sed 's/old_word/new_word/n' filename
```

Use the '/1', '/2' etc. flags to replace the first, second occurrence of a pattern in a line. The following command replaces the second occurrence:

```
sed 's/unix/linux/2' file.txt
```

Output:

```txt
unix is great os. linux is opensource. unix is free os.  
learn operating system.  
unix linux which one you choose.  
unix is easy to learn.linux is a multiuser os.Learn unix .unix is a powerful.
```

#### 3. Replacing all occurrences of a pattern

We can use `/g` to replace all occurences of a pattern in a line:

```bash
sed 's/unix/linux/g' file.txt
```

Output:

```txt
linux is great os. linux is opensource. linux is free os.  
learn operating system.  
linux linux which one you choose.  
linux is easy to learn.linux is a multiuser os.Learn linux .linux is a powerful.
```

#### 4. Replacing the nth occurrence to all occurrences in a line:

We can use a combination of `/1`, `/2` etc. and `/g` to replace all patterns from the nth occurrence of a pattern in a line. For instance, we can replace the third, fourth, fith, ..."unix" word to "linux" in a line:
```bash
sed 's/unix/linux/3g' geekfile.txt
```

Output:

```
unix is great os. unix is opensource. linux is free os.  
learn operating system.  
unix linux which one you choose.  
unix is easy to learn.unix is a multiuser os.Learn linux .linux is a powerful.
```

#### 5. Parenthesize first character of each word

The following example prints the first character of every word in parenthesis:

```bash
echo "Welcome To My Project" | sed 's/\(\b[A-Z]\)/\(\1\)/g'
```

Output:

```txt
(W)elcome (T)o (M)y 
```



#sed #commands 
