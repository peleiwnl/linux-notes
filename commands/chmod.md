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
chmod ugo-rwx text3.txt
```

The code revokes all the read(r), write(w) and execute(x) permissions from all user(u), group(g), and others(o) for the file text3.txt which results in this:

![[chmod removing permissions with symbolic notation.png]]

#### Example 2 - Adding read and write permissions to both user and group, and revoke execute permission from others for the file text3.txt

```
chmod ug+rw, o-x text3.txt
```

### Octal Notations Permissions in Linux

The octal notation is for representing file permissions in Linux by using three user groups by denoting 3 digits i.e.:
- user
- group
- other users

Here's how the permissions are mapped:
- Read(r) = 4
- Write(w) = 2
- Execute(x) = 1

Permissions for owner, group, and others are represented by a three-digit octal value. The sum of permissions for each group gives the corresponding number.

#### Reference:

```
chmod o
```

Now we type '+' for adding a permission:

```
chmod o+
```

Then type an 'x' for "executing" a permission:

```
chmod o+x
```

Then specify what we are changing:

```
chmod o+x text3.txt
```

Multiple permissions can also be changed at once, similar to symbolic notation.

Octal notations can be used like this:

![[octal notations.png]]

Using the octal notations table instead of 'r', 'w', and 'x'. Each digit octal notation can be used for either of the group 'u', 'g', or 'o'.




#commands #permissions