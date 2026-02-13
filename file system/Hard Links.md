
Each hard linked file is assigned the same lnode value as the original, therefore they reference the same physical file location. Hard links are more flexible and remain linked even if the original or linked files are moved throughout the file system, although hard links are unable to cross different file systems.

- [[ls]] [[-l]] command shows all the links with the link column shows number of links
- Links have actual file contents
- Removing any link just reduces the link count, but doesn't affect other links
- Even if we change the filename of the original file them also the hard links properly work
- We cannot create a hard link for a directory to avoid recursive loops.
- If original file is removed then the link will still show the content of the file
- The size of any of the hard link file is the same as the original file and if we change the content in any of the hard links, then the size of all hard link files are updated.
- The disadvantage of hard links is that it cannot be created for files on different file systems, and it cannot be created for special files or directories.
- To create a hard link is:

```
$ ln [original filename] [link name]
```