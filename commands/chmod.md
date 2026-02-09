## Change mode

A command used for changing file access permissions.

- `chmod +rwx filename` - Adds read, write and execute permissions
- `chmod -rwx directoryname` - Removes all permissions
- `chmod +x filename` - Grants executable permission
- `chmod -wx filename` - removes write and execute rights

Permissions can be modified using symbolic notation or octal notation.

### Symbolic Notation

Allows you to add, remove, or set permissions for specific users.

#### Example 1 To Change File Permission

Giving "execute" permissions to the world ("other") for the file "xyz.txt", we start by typing:

```
chmod o
```

Adding a '+' to say that you are "adding" permission.

```
chmod o+
```

Then type an 'x' to say you are adding "execute" permission:

```
chmod o+x
```

Finally, specify which file you are changing:

```
chmod o+x xyz.txt
```

![[chmod Symbolic Notation.png]]

You can also change multiple permissions at once. For example, taking all permissions away from everyone, you'd type:

```
chmod ugo-rwx xyz.txt
```

The code 


#commands #permissions