
We can use certain comparators within strings:

| Operator | Description                   |
| -------- | ----------------------------- |
| ==       | True if strings are equal     |
| !=       | True if strings are not equal |
| -n       | True if string is not null    |
| -z       | True if string is null        |

Arithmetic operators are used for checking the arithmetic-based conditions. Like less than, greater than, equals to, etc:

| Operator | Description           |
| -------- | --------------------- |
| -eq      | Equal                 |
| -ge      | Greater Than or Equal |
| -gt      | Greater Than          |
| -le      | Less than or Equal    |
| -lt      | Less than             |
| -ne      | Not Equal             |

## Example Script

```bash
if [10 -eq 10 ]; then
echo "Equal"
fi

if [ 'Geeks' == 'Geeks' ];
then
	echo "same" #output
else
	echo "not same"
fi
```

### Output

```
Equal
same
```

#shellscripting 