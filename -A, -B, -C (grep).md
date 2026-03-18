`-A` prints the searched line and n lines after the result. `-B` prints the searched line and n lines before the result, and `-C` prints the search line and n lines after and before the result.

## Syntax

```bash
grep -A[NumberOfLines(n)] [search] [file]
grep -B[NumberOfLines(n)] [search] [file]
grep -C[NumberOfLines(n)] [search] [file]
```

### Example:

```
grep -A "Pyt"
```


#flags #grep 