awk is a powerful text-processing command for analysing, filtering, and manipulating structured data like logs and CSV files. It scans input line by line and performs actions based on patterns and fields.

- Processes text column-wise using fields  (e.g. $1, $2)
- Ideal for parsing logs, reports, and delimited files
- Supports conditions, loops, and built-in functions
- Used in shell scripts and data processing pipelines

## Example

The following text file is used as the input file for all cases below:

### Command:

```bash
$cat employee.txt 
```

### Output:

![file](https://media.geeksforgeeks.org/wp-content/uploads/20251106153501033582/file.webp "Click to enlarge")

### Print All Lines (Default Behavior)

By default Awk prints every line of data from the specified file.  

****Command:****

$ awk '{print}' employee.txt

****Output:****  

![file](https://media.geeksforgeeks.org/wp-content/uploads/20251106153500945201/file.webp "Click to enlarge")

There is no pattern given. So the actions are applicable to all the lines. Action print without any argument prints the whole line by default, so it prints all the lines of the file without failure.

## Syntax

awk [options] 'pattern {action}' input-file > output-file

- ****awk:**** Starts the AWK text-processing program
- ****[options]:**** Controls AWK behavior (e.g., -F to set field separator)
- ****pattern:**** Specifies which lines to process (condition or regex)
- ****{action}:**** Defines what to do with matching lines (usually print)
- ****input-file:**** File that AWK reads line by line
- ****> output-file:**** Redirects processed output into a file

## Common awk Command Options

### 1. Using -F (Field Separator Option)

- The -F option sets a custom field separator.
- By default, fields are separated by spaces, but we can change this using -F.

****Example:**** Use Space (default separator)

awk -F' ' '{print $1, $4}' employee.txt

****Output:****

![file](https://media.geeksforgeeks.org/wp-content/uploads/20251106153500810344/file.webp "Click to enlarge")

Here,

- -F ' ' tells AWK to use space as a separator.
- $1 = first column (Name)
- $4 = fourth column (Salary)

### 2. Using -f (Program File Option)

You can write your AWK code in a file and execute it with -f.

****Example:**** Create a script file named print_salary.awk:

{ print $1, "has salary", $4 }

![file](https://media.geeksforgeeks.org/wp-content/uploads/20251106153500869614/file.webp "Click to enlarge")

- Run it using:

awk -f print_salary.awk employee.txt

****Output:****

![file](https://media.geeksforgeeks.org/wp-content/uploads/20251106153500657870/file.webp "Click to enlarge")

- The program file is executed for every line of the input file.

### 3. Using -v (Variable Assignment Option)

The -v option lets you define variables before AWK begins processing.

****Example 1:**** Define a Custom Message

awk -v msg="Employee Details:" 'BEGIN {print msg}'

****Output:****

![file](https://media.geeksforgeeks.org/wp-content/uploads/20251106153500728777/file.webp "Click to enlarge")

- awk -v msg="Employee Details:" defines a variable and prints it before processing starts.

****Example 2:**** Use Variable in Condition

awk -v limit=40000 '$4 > limit {print $1, $4}' employee.txt

****Output:****

![awk-v-limit](https://media.geeksforgeeks.org/wp-content/uploads/20260317191133303395/awk-v-limit.webp "Click to enlarge")

- The variable limit is assigned value 40000.
- The command prints employees whose salary is greater than 40000.

## Built-In Variables In Awk

Awk's built-in variables include the field variables—$1, $2, $3, and so on ($0 is the entire line) - that break a line of text into individual words or pieces called fields.

### 1. $0, $1, $2, ...

- $0 represents the entire input line, while $1, $2, $3, etc. represent individual fields (columns).
- Fields are automatically split based on the field separator (space by default).

### 2. NR (Number of Records)

- Keeps track of the current line number being processed.
- Increments automatically for each new record (line) read by AWK.

### 3. NF (Number of Fields)

- Stores the total number of fields in the current line.
- Commonly used to access the last field using $NF.

### 4. FS (Field Separator)

- Defines the character used to split fields in the input.
- Default is whitespace (spaces or tabs), but it can be changed (e.g., comma for CSV files).

### 5. RS (Record Separator)

- Specifies how input records are separated.
- Default is a newline character, meaning each line is one record.

### 6. OFS (Output Field Separator)

- Controls the separator used between fields in output.
- Default is a space and is applied when using commas in print.

### 7. ORS (Output Record Separator)

- Defines how output lines are separated.
- Default is a newline, and it is automatically added after each print.

## More Examples of the awk command

### 1. Search Lines with a Keyword

It is used to find and print every line in the employee.txt file that contains the word "manager."

****Command:****

$ awk '/manager/ {print}' employee.txt 

****Output:****  

ajay manager account 45000  
varun manager sales 50000  
amit manager account 47000 

- The awk command prints all the line which matches with the ‘manager’. 

### 2. Print Specific Columns

For each record i.e line, the awk command splits the record delimited by whitespace character by default and stores it in the $n variables. If the line has 4 words, it will be stored in $1, $2, $3 and $4 respectively. Also, $0 represents the whole line.

****Command:****

$ awk '{print $1,$4}' employee.txt 

****Output:****  

ajay 45000  
sunil 25000  
varun 50000  
amit 47000  
tarun 15000  
deepak 23000  
sunil 13000  
satvik 80000 

- $1 and $4 represents Name and Salary fields respectively. 

### 3. Use of NR built-in variables (Display Line Number) 

It is used to add line numbers to each line of the employee.txt file and then print the numbered lines to the standard output (your terminal).

****Command:****

$ awk '{print NR,$0}' employee.txt 

****Output:****  

1 ajay manager account 45000  
2 sunil clerk account 25000  
3 varun manager sales 50000  
4 amit manager account 47000  
5 tarun peon sales 15000  
6 deepak clerk sales 23000  
7 sunil peon sales 13000  
8 satvik director purchase 80000 

- The awk command with NR prints all the lines along with the line number. 

### 4. Use of NF built-in variables (Display Last Field) 

****Command:****

$ awk '{print $1,$NF}' employee.txt 

****Output:****  

ajay 45000  
sunil 25000  
varun 50000  
amit 47000  
tarun 15000  
deepak 23000  
sunil 13000  
satvik 80000 

- $1 represents Name and $NF represents Salary. We can get the Salary using $NF , where $NF represents last field. 

### 5. Another use of NR built-in variables (Display Line From 3 to 6)

It is used to print specific lines (from line 3 to line 6, inclusive) of a file named employee.txt, along with their corresponding line numbers.

****Command:****

$ awk 'NR==3, NR==6 {print NR,$0}' employee.txt 

****Output:****  

3 varun manager sales 50000  
4 amit manager account 47000  
5 tarun peon sales 15000  
6 deepak clerk sales 23000 

For the given text file:  

****Command:****

cat geeksforgeeks.txt

****Output:****

A    B    C  
Tarun    A12    1  
Man    B6    2  
Praveen    M42    3

## AWK Built-in Variables

### 1) To print the first item along with the row number(NR) separated with ” - “ from each line in geeksforgeeks.txt

It is used to read a file line by line, prefix each line with its line number, and then print only the line number followed by the first word of that line.

$ awk '{print NR "- " $1 }' geeksforgeeks.txt

****Output:****

1 - A  
2 - Tarun  
3 – Manav      
4 - Praveen

### 2) To return the second column/item from geeksforgeeks.txt:

****Command:****

$ awk '{print $2}' geeksforgeeks.txt

****Output:****

B  
A12  
B6  
M42

### 3) To print any non empty line if present

It is used to process the file geeksforgeeks.txt, but it will not produce any output.

****Command:****

$ awk 'NF < 0' geeksforgeeks.txt

here NF should be 0 not less than and the user have to print the line number also:

correct answer : awk 'NF == 0 {print NR}'  geeksforgeeks.txt

OR 

awk 'NF <= 0 {print NR}'  geeksforgeeks.txt

****Output:****

0

### 4) To find the length of the longest line present in the file

It is used to find and print the length of the longest line in the file named geeksforgeeks.txt.

****Command:****

$ awk '{ if (length($0) > max) max = length($0) } END { print max }' geeksforgeeks.txt

****Output:****

13

### 5) To count the lines in a file

It is used to count and print the total number of lines in a file.

****Command:****

$ awk 'END { print NR }' geeksforgeeks.txt

****Output:****

3

### 6) Printing lines with more than 10 characters

It is used to filter and print only those lines from geeksforgeeks.txt that have more than 10 characters.

****Command:****

$ awk 'length($0) > 10' geeksforgeeks.txt

****Output:****

Tarun    A12    1  
Praveen    M42    3

### 7) To find/check for any string in any specific column

It is used to find and print every line from the file geeksforgeeks.txt where the third piece of data (or column) in that line is exactly "B6".

****Command:****

$ awk '{ if($3 == "B6") print $0;}' geeksforgeeks.txt

### 8) To print the squares of first numbers from 1 to n say 6

This command is used to generate and print the squares of numbers from 1 to 6.

****Command:****

$ awk 'BEGIN { for(i=1;i<=6;i++) print "square of", i, "is",i*i; }'

****Output:****

square of 1 is 1  
square of 2 is 4  
square of 3 is 9  
square of 4 is 16  
square of 5 is 25  
square of 6 is 36

test
test
test
test
