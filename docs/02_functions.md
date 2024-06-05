# Functions and variables
Just like pushing values to the stack, calling functions is just as simple syntax-wise.
You just write the name of the function, like this:

```
2 3 +
```

This calls the `+` function.

## Defining functions
Defining functions uses this syntax:

```
func functionName begin
	...
end
```

Where `functionName` is the name of the function. Where `...` is, you can write the code
that runs in your function. To get the parameters of your function, you can either operate
on them using the stack, or save them in variables to make things easier. This is how you
do that with variables, for a function with 2 parameters:

```
func foo begin
	let cell bar
	let cell baz

	baz !
	bar !
end
```

The `let` statement declares a variable. The part of the statement saying `cell` is the
type of the variable. The `cell` type is an integer type that is as big as stack cells
(a cell is a value on the stack). After that, there is the variable's name.

After that, the function saves the parameters in the functions. First, it pops a value
into the `baz` variable, then pops into the `bar` variable. Writing variable names in
Callisto pushes the address of that variable to the stack. The `!` function takes an
address and a value from the stack and writes the value to that address as a cell.

If you need to get the value of these variables, you can use the `@` function. It pops
an address from the stack, reads a value from that address, and then pushes that value
to the stack. For example:

```
let cell ch
'A' ch !

ch @ printch
```

The `printch` function pops a character from the stack and prints it.

You can also create constant variables like this:

```
const name value
```

Where `name` is the name of the constant and `value` is the value of the constant.
Writing the name of a constant will push the value of that constant to the stack.

All of the functions so far are apart of Callisto's core library. This library contains
platform dependant code written in Assembly that make up simple operations. These operations
are used to build a full platform independant standard library.

## More info
- [Functions](https://callisto.mesyeti.uk/docs/language/functions/)
- [Variables](https://callisto.mesyeti.uk/docs/language/variables/)
- [Core library](https://callisto.mesyeti.uk/docs/core/core/)
