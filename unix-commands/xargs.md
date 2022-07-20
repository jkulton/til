# xargs

The `xargs` utility reads space, tab, newline and end-of-file delimited strings from the standard input and executes utility with the strings as arguments.

Any arguments specified on the command line are given to utility upon each invocation, followed by some number of the arguments read from the standard input of `xargs`. This is repeated until standard input is exhausted.

```
$ touch 1.txt 2.txt 3.txt
$ ls
1.txt 2.txt 3.txt index.html
$ ls *.txt | xargs rm
$ ls
index.html
```
