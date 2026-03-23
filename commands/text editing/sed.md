## Stream editor

A non-interactive text editor for performing basic text transformations on an input stream, such as a file or input from a pipeline. It processes text line by line and applies the editing commands you specify.

It can:

![[sed commands image.png]]

`sed` works with two workspaces: The pattern space holding the line being modified, and the hold space which can temporarily store a line for later use.

### Syntax

```bash
sed [OPTIONS] 'COMMAND' [INPUTFILE...]
```

Where:
- OPTIONS: Optional flags for modifying behaviour
- COMMAND: The command/sequence of commands to execute on the input file
- INPUTFILE: One or more input files to be processed

### Common Flags

- [[-i (sed)]]
- [[-n (sed)]]
- [[-e (sed)]]
- [[-f (sed)]]
- [[-r (sed)]]