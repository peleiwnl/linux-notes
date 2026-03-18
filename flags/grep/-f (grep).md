Used to search for multiple patterns, listed in a separate file, within another target file.

Command:
```bash
grep -f pattern.txt file.txt
```

- `-f pattern.txt` tells `grep` to read patterns from the file `pattern.txt`, one pattern per line (each line is treated as a pattern/regular expression)
- `grep` then searches `file.txt` and prints lines from `file.txt` that matches any of the patterns in `pattern.txt`

## Output:
### pattern.txt

```bash
Agarwal
Aggarwal
Agrawal
```

### file.txt
```bash
Raj Agarwal
Suman Aggarwal
Kiran Agrawal
```


#flags #grep 