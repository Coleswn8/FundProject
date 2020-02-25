# MathLang: Programming Language Fundamentals Project
A stack-based language that performs basic mathematic/logic operations.

## Team Members
Name			 | ONID Username
:---------------:|:--------------:
Melanie Gutzmann | gutzmanm
Cole Swanson     | swanscol
Hannah Vaughan   | vaughanh

## Language Introduction
Our language, named _MathLang_, is a stack-based language with a stack that can have integers, booleans, and tuples as its values. These values can be pushed onto the stack, and mathematical operations can be performed on the integer values in the stack. Conditional logic allows for differing series of commands to be executed with if/else branching; while loops allow for looping to occur on values on the stack, and tuples can be both constructed and deconstructed to provide invertability.

## Usage
### Setup Instructions
_MathLang_ is intended to be run from GHCi, so the _Lang_ module must be loaded to run programs in the language.

### Good Program Examples and their Outputs
```haskell
cmd Push (I 4) []
>>> Expected Output: Just [I 4]
```

```haskell
cmd Push (B True) [I 4]
>>> Expected Output: Just [I 4, B True]
```

```haskell
cmd Push (T (I 1) (B False)) [I 4, B True]
>>> Expected Output: Just [I 4, B True, T (I 4) (B False)]
```

```haskell
cmd E Add [I 2, I 3, B True]
>>> Expected Output: Just [B True, I 5]
```

```haskell
cmd S (While Equ S (Begin [Push (I 3), Push (I 2), Mul])) [B True, B True]
>>> Expected Output: Just [6]
```

```haskell
cmd Push (I 4) []
>>> Expected Output: Just [I 4]
```

```haskell
cmd Push (B True) [I 4]
>>> Expected Output: Just [I 4, B True]
```

```haskell
cmd Push (T (I 1) (B False)) [I 4, B True]
>>> Expected Output: Just [I 4, B True, T (I 4) (B False)]
```

```haskell
cmd E Add [I 2, I 3, B True]
>>> Expected Output: Just [B True, I 5]
```

```haskell
cmd S (While Equ S (Begin [Push (I 3), Push (I 2), Mul])) [B True, B True]
>>> Expected Output: Just [6]
```

```haskell
cmd Push (I 4) []
>>> Expected Output: Just [I 4]
```

```haskell
cmd Push (B True) [I 4]
>>> Expected Output: Just [I 4, B True]
```

```haskell
cmd Push (T (I 1) (B False)) [I 4, B True]
>>> Expected Output: Just [I 4, B True, T (I 4) (B False)]
```

```haskell
cmd E Add [I 2, I 3, B True]
>>> Expected Output: Just [B True, I 5]
```

```haskell
cmd S (While Equ S (Begin [Push (I 3), Push (I 2), Mul])) [B True, B True]
>>> Expected Output: Just [6]
```

```haskell
prog [Push (I 2), Push (I 3), Add] []
>>> Expected Output: Just [5]
```

```haskell
prog [Push (I 1), Push (I 2), E Add, Push (B True), Push (B True), E Equ] []
>>> Expected Output: Just [B True,I 3]
```