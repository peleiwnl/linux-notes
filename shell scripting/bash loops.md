
Loops allow us to automate repetitive tasks by running a block of code multiple times. Loops can be used for all sorts of common tasks.


## While statement

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

Note: [[exp]] is used for arithmetic expressions
#### Output:

![[bash while loop example.png]]