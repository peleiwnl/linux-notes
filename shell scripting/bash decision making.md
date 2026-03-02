
Conditions can be provided for the execution of a block of code. If met, only one condition gets executed.

## If-Else Statement:

Can be used to execute two different codes based on whether the condition is met or not.

There are a few varieties:
- If-fi
- if-else-fi
- if-elif-else-fi
- nested if-else

The syntax for the simplest one is:

### 1. Syntax of lf-else statement:

```
if [ expression ]; then

	statements
	
	
```

#### Example

```
Name="James"
if [ "$Name" = "James" ]; then
	echo "His name is James. It is true"
```

### Output of if-else statement

```
His name is James. It is true
```

### 2. Case-sac statement

```bash
case $var in
	Pattern 1) Statement 1;;
	Pattern n) Statement n;;
esac
```

### Example

```bash
Name="James"
case "$Name" in
	#case 1
	"Ben") echo "Profession: Builder" ;;
	
	#case 2
	"Will") echo "Profession: Developer" ;;
	
	#case 3
	"James") echo "Profession: Writer" ;;
esac
```

### Output

```bash
Profession: Writer
```

