## Change ownership

This command changes the ownership of files or directories to a specific user or group. 

- Changes the file owner and group simultaneously or individually
- Only the root user or file owner (with permissions) can change ownership
- Use` chown user file` to change only the owner
- Use` chown :group file `to change only the group
- Use `chown -R user:group directory/` for recursive ownership changes. `chmod +rwx filename` - Adds read, write, and execute permissions.

### Basic Example

```
chown vboxuser sample.txt
```

### Syntax

```
chown [options] new_owner[:new_group] file(s)
```

A breakdown:
- `chown`: The base command
- `options`: Optional flags that modify the behaviour of the `chown` command.
- `new_owner[:new_group]:` The new owner and optionally the new group if `new_group` is omitted, only the owner is changed.
- `file(s)`: The file or files for which ownership is to be changed.

### Changing the Group of a File

#### Syntax:

```
chown :group1 file1.txt
```

`group1` is assigned as the new group for the file `file1.txt` - Useful for managing access permissions within specific groups.

### Changing the Owner and Group of the File in Linux

#### Syntax:

```
chown master:group1 file1.txt
```

### Changing Group Ownership

#### Syntax:

```
chown :group1 file1.txt
```

### Changing Owner as well as Group

```
chown master:group1 greek1
```

Here, greek1 is a file.

### Changing Owner from a Particular Ownership only

#### Syntax:

```
chown --from=master root greek1
```

### Changing Group from a Particular Group

#### Syntax:

```
chown --from-:group1 root greek1
```

### Copying Ownership of One File to Another

#### Syntax:

```
chown --reference=greek1 greek2
```

### Changing Owner of Mul

#commands #permissions 