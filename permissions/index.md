Linux file permissions are the foundation of the system's security model, defining who can read, write, or execute files and directories, ensuring only authorized users or processes can access sensitive data.

These can be modified using the [[chmod]] command.

## The Three Basic Permissions

Every file or directory has three types:
- [[read]] (r)
- [[write]] (w)
- [[execute]] (x)

| Letters | Definition                                                                  |
| ------- | :-------------------------------------------------------------------------- |
| 'r'     | "read" the file's contents.                                                 |
| 'w'     | "write", or modify, the file's contents.                                    |
| 'x'     | "execute" the file. This permission is given only if the file is a program. |
## Ownership and Permission groups

Permissions are assigned to three categories of users:
- [[user]] (owner)
- [[group]]
- [[others]]

| Operators | Definition                                  |
| --------- | :------------------------------------------ |
| '+'       | Add permissions                             |
| '-'       | Remove permissions                          |
| '='       | Set the permissions to the specified values |
### What are Permission Groups?

Each of the three "rwx" characters refers to a different operation you can perform on the file.

1. <span style="color:rgb(24, 205, 136)">Owners</span>: These permissions apply exclusively to the individuals who own the files or directories. 
2. <span style="color:rgb(24, 205, 136)">Groups</span>: Permissions can be assigned to a specific group of users, impacting only those within that particular group.
3. <span style="color:rgb(24, 205, 136)">All Users</span>: These permissions apply universally to all users on the system, presenting the highest security risk.

Assigning permissions to all users should be done cautiously to prevent security vulnerabilities.

### User, Group, and others Option in Linux File Permission

| Reference | Class     | Description                                                                                                                                    |
| --------- | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| 'u'       | user      | The user permissions apply only to the owner of the file or directory, they will not impact the actiions of other users                        |
| 'g'       | group     | The group permissions apply only to the group that has been assigned to the file or directory, they will not affect the actions of other users |
| 'o'       | others    | The other permissions apply to all users on the system. this is the permission group which needs to be watched the most                        |
| 'a'       | all three | All three (owner, groups, others)                                                                                                              |

## Checking the Permission of Files in Linux

### The "Trusty Command"

#### Input:

```
ls -l text1.txt
```

#### Output:

```
-rw-r--r-- 1 user group 46 Apr 14 16:37 text1.txt
```

This command represents the following information:

1. The first character = "-", meaning it's a file 'd', which is a directory.
2. The next nine characters = (rw-r--r--) show the security
3. The next column shows the owner of the file.
4. The next column shows the group owner of the file (which has special access to these files)
5. The next column shows the size of the file in bytes.
6. The next column shows the date and time the file was last modified.

### The 'namei' Command

The 'namei' command is used to check the file path through layer of folder's path:

```
namei -l /path/to/your/file
```

### The 'stat' command

Used to pin point the file location.

```
stat text1
```

#### Output:

```
  File: example.txt  
  Size: 2210       Blocks: 8          IO Block: 4096  regular file  
Device: 802h/2050d    Inode: 1288496     Links: 1  
Access: 2024-11-18 10:50:56.000000000 +0000  
Modify: 2024-11-18 10:50:56.000000000 +0000  
Change: 2024-11-18 10:50:56.000000000 +0000  
 Birth: -
```


## Changing Permissions in Linux

Refer to [[chmod]].





#permissions #permissiongroups 