# The stack and operations
Callisto has 2 stacks: the data stack and the return stack. The return stack isn't available
for the programmer to use (for now). A stack is like an array that you can push to (add to
the top), or pop from (remove from the top).

In Callisto, you can push integers to the array by just writing the integer, like this:

```
16 39 40
```

This will push 16, 39, and 40 to the stack, with 40 at the top of the stack.

The stack is used everywhere in Callisto: for passing parameters, returning values, or
even temporary data. This is what makes the language stack-based. Functions in Callisto
take parameters from this stack and return values by pushing to it. For example, if you
had the following stack:

```
2 3
```

The `+` would pop these two values, and then push `5` to the stack, resulting in this
stack:

```
5
```


