## Checking whole words using grep

By default, grep matches the given string/pattern even if its found as a substring in a file. The -w option to grep makes it match only the whole words.

```bash
grep -w "Python" grepexample1.txt
``` 

Output:

![[grep -w example.png]]

