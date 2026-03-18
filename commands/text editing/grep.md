The grep command is used to search for specific words, phrases, or patterns inside text files, and shows the matching lines on screen. It is useful for finding keywords or phrases in logs or documents.

## Search for a word in a file

If we have a file called `notes.txt` and want to find all lines containing the word Python, you can use:

```
grep "python" notes.txt
```

The output would be:

![[using grep to search for a word example.png]]

## Syntax of the `grep` command in Unix/Linux

The basic syntax is:
```bash
grep [options] pattern [files]
```

- `[options]` - Command-line flags modifying the behaviour of `grep`
- `[pattern]` - Regular expression we want to search for
- `[file]` - The name of the file(s) you want to search within. You can specify multiple files for simultaneous searching.
## Commonly Used `grep` Options

### Flags

#### Case Insensitivity 
- See [[-i]]

#### Displaying count matches
- See [[-c]]




#textediting #grep

