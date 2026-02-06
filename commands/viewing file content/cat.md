## Concatenate

Used to view, create, and combine file contents directly from the terminal. It allows users to quickly work with file content without opening a text editor.

- Can concatenate multiple files and display them as a single continuous output
- Helps in creating new files or appending data to existing ones
- Useful for quick file inspection, debugging, and scripting tasks without opening a text editor.

### Syntax of cat Command

The basic syntax of the cat command is as follows:

```
cat [options] file_name
```

- `[options]`: Additional flags to modify the behaviour of the command.
- `[file_name]`: One or more files to read, create, or combine.

### Flags

- [[-n]] View File Content with Line Numbers
- [[-s]] Suppress Repeated Empty Lines
- [[-E]] Highlight End of Each Line
- [[-A]] Display Non-Printing Characters
- [[--]] Open Files Whose Names Start with a Dash

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
cat testtext1.txt testtext2.txt
```

![[cat view the content of multiple files in linux.png]]

#### 4. Create a New File and Add Content Using cat Command

The cat command can also be used to create a new file or overwrite an existing file with new content using output redirection (<span style="color:rgb(24, 205, 136)">></span>):

##### Syntax:

```
cat > file_name
```

- Type your content
- Press Ctrl + D to save and exit

##### Example:

If we want to create a new file named text1:

```
cat > text1
```

This allows you to type directly into the terminal, and once you press Ctrl + D, the entered text is saved into text1.

![[cat creating a new file and adding content.png]]

#### 5. Copy or Merge File Contents Using cat Command

The `cat` command can combine the content of one or more files and redirect it into another file using >.
##### Syntax:

```
cat file1 file2 > new_file
```

##### Example:

```
cat file1.txt file2.txt > merged_file.txt
```

![[cat copy or merge file contents example.png]]

#### 6. Merge Contents of Multiple Files into a Single File

The cat command can merge the contents of multiple files and store them into a new file using the direction operator (>). This is useful when combining logs, text data, or documentation files.

##### Syntax:

```
cat file1 file2 file3 > merged_file
```

##### Example:

```
cat "text1" "text2" "text3" > "merged123"
```

![[cat merge contents of multiple files into a single file example.png]]

This will combine the contents of file1.txt, file2.txt and file3.txt and save them into merged123.txt

#### 7. Append the Content of One File to Another File

The append operator <span style="color:rgb(24, 205, 136)">>></span> is used along with the cat command to add the content of one file to the end of another file

##### Syntax:

```
cat file_name1 >> file_name2
```

##### Example:

```
cat file1 >> file2
```

![[cat append the content of one file to another file example.png]]

This will append the content of file1.txt to the end of file2.txt


#### 8. Append Content to an Existing File Using cat Command

The cat command can new text to an existing file using the append redirection operator 

#commands #cat 
