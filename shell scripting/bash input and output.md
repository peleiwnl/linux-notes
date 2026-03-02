
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