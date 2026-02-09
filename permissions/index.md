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


#permissions #permissiongroups 