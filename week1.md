# Lab Report 1 - Remote Access and FileSystem (Week 1)
## Directory Structure

The directory structure we'll be using:
```zsh
> tree
.
├── cse15l-lab-reports-fa23
│   ├── index.md
│   └── week1.md
└── lecture1
    ├── Hello.java
    ├── README
    └── messages
        ├── en-us.txt
        ├── es-mx.txt
        └── zh-cn.txt
```

## `cd`: Change Directory

### with no arguments

When we type in `cd` without an argument, we return to the home directory.

This probably happened because `cd` will interpret the text after it as the directory destination the user wants to change to. Thus, when the text after `cd` is blank, it interprets that as going to the home directory.

```zsh
❯ pwd # Print our current working directory
/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L
❯ cd # Change directory without argument
❯ pwd # Print our current working directory
/Users/chen_yenru
```

### with a path to a directory as an argument.

In the example below, we used `cd lecture1` with the argument `lecture1`. And `cd` interprets it as changing the directory from our current working directory (`/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L`) to its subdirectory `lecture1`. This makes the absolute path now `/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L/lecture1`.

```zsh
❯ pwd # Print our current working directory
/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L
❯ ls
cse15l-lab-reports-fa23 lecture1
❯ cd lecture1
❯ ls
Hello.java README messages
❯ pwd
/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L/lecture1
```

### with a path to a file as an argument.

In the example below, we have the working directory `/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L/lecture1`. Within `lecture1`, there is `Hello.java`, `README`, and `messages/`.

We entered `cd Hello.java`, which uses the file `Hello.java` as the argument of `cd`.

What happened?

The terminal returned `cd: not a directory: Hello.java`.

And this is because when we use `cd`, the argument after it should be the name of a directory that exists in the path. And since `Hello.java` is not a directory, it does work.


```zsh
❯ pwd
/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L/lecture1
❯ ls
Hello.java README messages
❯ cd Hello.java
cd: not a directory: Hello.java
```


## `ls`: List 
### with no arguments

In the example below, we have the working directory `/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L`.

When we type in `ls` without argument, the terminal returned the file and subdirectory within the working directory.

```zsh
❯ ls
cse15l-lab-reports-fa23 lecture1
```
### with a path to a directory as an argument.
In the example below, we have the working directory `/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L`.

When we type in `ls` with the argument `lecture1` (which is a subdirectory in our working directory), the terminal returns the files and subdirectories inside `lecture1`.

The `ls` command might have interpreted the argument as the directory to instead start with in listing content. 

```zsh
❯ ls lecture1/
Hello.java README     messages
```


### with a path to a file as an argument.

In this example below, we are in the working directory `/Users/chen_yenru/Documents/GitHub/SCHOOL/UCSD/FA2023/CSE15L/lecture1`.

When we type in `ls` with the argument `README` (which is a file in our working directory), the terminal returns the file's name.

This might have happened because when the argument is a filename, `ls` lists the file's name in return.

```zsh
❯ ls README
README
```
## `cat`: Concatenate
### with no arguments
### with a path to a directory as an argument.
### with a path to a file as an argument.