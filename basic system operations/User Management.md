
User management is a core function of Linux system administration, controlling system access, enforcing security, and ensuring users have correct privileges. 

Efficient user management:
- Secures the system from unauthorized access
- ensures users can perform their roles without interfering with others
- Helps in auditing and tracking user activity

## Understanding User IDs (UIDs)

Linux supports up to 60,000 users, suitable for large-scale use.

![[Linux User Ids.png]]

Admins can create, modify, delete accounts, set permissions, and enforce access policies to ensure System integrity.

### Types of Users in Linux

Linux is a multi-user OS, meaning multiple users can access and operate the system simultaneously. Here are the main types of users:

| User Type              | Description                                                                                             |
| ---------------------- | ------------------------------------------------------------------------------------------------------- |
| Root (Superuser)       | Full system control. Can install software, change config files, and delete anything. Powerful but risky |
| Regular User           | Limited access. Can create files, run applications, but not modify system-level settings.               |
| Sudo User              | Regular user with temporary admin rights via the sudo command,                                          |
| System/Service Account | Non-human accounts used by services (e.g. mysql). Limited privileges                                    |
| Guest User             | Temporary users with minimal privileges. Changes are not saved after logout.                            |

## User Groups

A user group is a collection of users. If you give permission to a group, all users in that group get the same access, making it easier to manage file and system permissions for many users at once.

### 1. Primary Group

- Every linux user is assigned one primary group
- When a user creates a file, the group ownership is set to their primary group
- By default, this usually has the same name as the user
- Helps manage file ownership cleanly without much extra configuration.

#### Example: Check Primary Group

```
id peleiwnl
```

#### Output:

![[check primary group example.png]]

### 2. Secondary Group (Additional Permissions)

- A user can be part of multiple secondary groups
- These groups provide extra access to files, folders or services
- Commonly used for team-based access or system-level permissions

...

## User Management Files

Essential for managing users, groups and permissions on a Linux system, and play a key role in ensuring security and efficient system administration.

![[User Management example.png]]

## User Account Management Commands

### 1. List all Users

To list all users, use the awk command with the -F option. 

### 3. Add a user

```
sudo useradd test_user
```

### 4. Assign a Password

```
passwd test_user password
```

### 5. Accessing a User Configuration File

To view the details from the `/etc/passwd` file, we can use the cat command. It will contain information like UID, GID, home directory and login shell.

![[accessing a user configuration file example.png]]

## Modify User information



