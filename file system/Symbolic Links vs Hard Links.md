A link in UNIX is a pointer to a file. Creating links are shortcuts to access a file, which allow more than one file name to refer to the same file elsewhere.

There are two types:

1. [[Soft Link or Symbolic links]]
2. [[Hard Links]]

They behave differently when the source of the link is moved or removed. Symbolic links are not updated, and hard links always refer to the source, even if moved or removed.

If we have a file a.txt, and create a hard link to the file and then delete it, we can still access the file using a hard link, but we cannot with a soft link and the soft link becomes dangling. Hard links increases the reference count of a location while soft links work as a shortcut.

