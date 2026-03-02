Variables are assigned by typing a String to represent them, and then called with the "$" symbol.

We can create variables when bash scripting. For example:
```bash
Name="James"
Age=20

echo "$Name, $Age"
```

Output:

```
James, 20
```


There are two types. If a variable is declared inside a function, it is a **local** variable, but if declared outside, then it is a global variable. By default, bash variables written inside or outside a function by default is global, but we can make it local by using the keyword "local".

#shellscripting 