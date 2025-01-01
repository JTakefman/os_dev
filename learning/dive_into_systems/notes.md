# Notes

## Chapter 7 x86-64 Assembly

### 7.1.1

%rsp: Stack Pointer, tracks top of stack (duh)

%rbp: Frame Pointer/Base pointer, tracks base of stack (duh). Not typcially used in x86-64.

%rdi, %rsi, %rdx, %rcx, %r8 and %r9: Typically used to store first six parameters.

%rax: Typically used to store the return value of a function

### 7.1.2

__Table for accessing lower bits of registers__