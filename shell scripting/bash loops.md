
Loops allow us to automate repetitive tasks by running a block of code multiple times. Loops can be used for all sorts of common tasks.


## While statements

If a condition is true, it'll run the condition until it is false.

```bash
#/bin/bash
while <condition>
do
	<command 1>
	<command 2>
	<etc>
done
```

### Example script: Printing the value of a

```bash
#/bin/bash
a=0
# lt is less than operator
#Iterate the loop until a less than 10
while [ $a -lt 10 ]
do 
    # Print the values
    echo $a
    # increment the value
    a=`expr $a + 1`
done
```

Note: [[expr]] is used for arithmetic expressions
#### Output:

![[bash while loop example.png]]


## For statements

The loop operates on a list of items, repeating a set of commands for every item on the list.

```bash
#/bin/bash
for <var> in <value1 value2 ... valuen>
do
	<command 1>
	<command 2>
	<etc>
done
```

Each time the loop executes, the value of the variable var is set to the next word in the list of words, word1 to wordN.

### Example script: Breaking the loop when a = 5

```bash
#/bin/bash
#Start of for loop
for a in 1 2 3 4 5 6 7 8 9 10
do
    # if a is equal to 5 break the loop
    if [ $a == 5 ]
    then
        break
    fi
    # Print the value
    echo "Iteration no $a"
done
```

#### Output:

![[bash for loop example.png]]

### Example: Using a continue statement in a for loop

Using the same script, we can add a continue instead of break:

```bash
#/bin/bash
for a in 1 2 3 4 5 6 7 8 9 10
do
    # if a = 5 then continue the loop and 
    # don't move to line 8
    if [ $a == 5 ]
    then 
        continue
    fi
    echo "Iteration no $a"
done
```

#### Output:

![[bash for loop continue example.png]]

## Until statements

The until loop is executed as many times as the condition/command evaluates to false, and will terminate when the condition/command becomes true.

### Syntax:

```bash
#/bin/bash
until <condition>
do
	<command 1>
	<command 2>
	<etc>
done
```

### Iteration until the value is greater than 10 example

```bash
#/bin/bash
a=0
# -gt is greater than operator
#Iterate the loop until a is greater than 10
until [ $a -gt 10 ]
do
    # Print the values
    echo $a
    # increment the value
    a=`expr $a + 1`
done
```

#### Output:

![[bash until loop example.png]]

## More examples of looping statements

### Example 1: Iterating over colours using a For Loop:

```bash
#/bin/bash
COLORS="red green blue"
# the for loop continues until it reads all the values from the COLORS  
for COLOR in $COLORS
do
    echo "COLOR: $COLOR"
done
```

