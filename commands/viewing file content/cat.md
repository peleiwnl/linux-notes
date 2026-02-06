## Concatenate

Used to view, create, and combine file contents directly from the terminal. It allows users to quickly work with file content without opening a text editor.

- Can concatenate multiple files and display them as a single continuous output
- Helps in creating new files or appending data to existing ones
- Useful for quick file inspection, debugging, and scripting tasks without opening a text editor.

### Examples

#### 1. View the Content of a Single File in Linux

To display the content of a single file in the terminal:

##### Syntax:

```
cat file_name
```

##### Example:

```
cat testtext.txt
```

![[cat viewing file content example.png]]

#### 2. View the Content of a File Using Full Path

We can also read a file using its complete path instead of just the file name

##### Syntax:

```
cat /path/to/filename
```

##### Example

```
cat /home/peleiwnl/test/testtext.txt
```


![[cat view content of a file using file path example.png]]

#### 3. View the Content of Multiple Files in Linux

The cat command can display the content of more than one file together. The output of the first file appears first, followed by the second file.

##### Syntax:

```
cat file_name1 file_name2
```

##### Example: 

```

```