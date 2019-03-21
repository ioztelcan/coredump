### To print the buffer in an array:
`x /100bx buf` -> Prints 100 bytes as hexadecimal.
`x /100bs buf` -> Prints 100 bytes as string

### Running a python file with gdb:
!!! Warning: This might only work with instantiations of c code within python.

 - Run `gdb python3`
 - Inside gdb `run ./python_file.py`


After this the symbols are added (I think) and you can put breakpoints, and run the same command.

-------------------------------------------------------
### Shortcuts:

backtrace:	bt
breakpoint: 	b <function_name or line_no> 
next:		n
step:  		s 
run:   		r 
continue: 	c
list: 		l

`Ctrl + X` and `Ctrl + A` right after, turns on/off tui. (text user interface)

### evaluate an expression and print the result
p length=strlen(string)
