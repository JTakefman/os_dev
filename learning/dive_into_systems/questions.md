# Questions

## Dec 28th, 2024:

### Q: Are the fixed-width integer types ie. `int_8`, `uint_32` a standard library feature or are they constructed using type defs?

### A: Both

Provided via the `<stdint.h>` header but also constructed in and for specific contexts ie. embedded libraries and so on.

## Dec 28th, 2024:

### Q: How does a compiler typically decide on the addresses for stack and heap? And particularly for the heap, is allocation sequential (I'd assume not)?

### A:

See gpt for full details


## Dec 30th, 2024:
### Q: Why the subtraction of 8 in the equivelant push and pop calls in x86 assembly? ie.
```
//Push
sub $0x8, %rsp
mov S, (%rsp)
```
and 
```
//Pop
mov (%rsp), D
add $0x8, %rsp
```

### A:
Remember that adresses __bytes not words and you store very important variable/piece of data as a full word__.
Thus you need to jump the full 8 bytes for each word.

### Q: How does x86 typically store arguments? Moreover

### A:

### Q: Does allocation for stack variables occur at compile or runtime?
I'd assume it has to be compile time because otherwise, how will a bare-metal/kernel-development context
like what I'm working on ever get them to occur? Though, I guess if we assume that the translation of the code
to assembly includes by it's nature the necessary calls to allocate the variables then it's fine.

I think maybe I'm thinking too much like an interpreter not a compiler.

### A:
Good job you thought it through lol.

