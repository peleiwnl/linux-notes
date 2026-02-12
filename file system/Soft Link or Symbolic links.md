Similar to the file shortcut feature used in Windows OS. Each soft linked file contains a separate Inode value that points to the original file. Similar to hard links, any changes to the data in either file is reflected in the other. Soft links can be linked across different file systems, although if the original is deleted or moved, the soft linked file will not work correctly.

- [[ls]] [[-l]] shows all links with first column value l? and the link points to the original file
- Soft Link contains the path for the original file and not the contents
- Removing a soft link doesn't affect anything, but when removing the original file, the link becomes "dangling", pointing to a non-existent file. 
- A soft link can link to a directory.
- The sizer of a soft link is equal to the length of the path of the original file we gave. E.g., if we link a file like `ln -s /tmp/hello.txt`, `/tmp/link.txt` is then the size of the file, which is 14 bytes.
- If we change the name of the original file, all soft links for that file become dangling i.e. they are worthless now. 
- Can be used to link across file systems.