
A script can take one or more inputs and can produce zero or many outputs. It may even produce some errors.

## Example

```bash
echo "Enter filename"
read filename

if [ -e $filename ]
then
echo "$filename exists in the directory"
cat $filename

else
	cat > $filename
	echo "File created"
fi
```

This will read a filename, if it exists it will print the output, if not it will take input from the user to create a file under the name they were searching for.

#shellscripting 