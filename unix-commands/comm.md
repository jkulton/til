# comm

The [`comm`](https://man7.org/linux/man-pages/man1/comm.1.html) utility can be used to compare two sorted files.

> With no options, produce three-column output.  Column one contains lines unique to FILE1, column two contains lines unique to FILE2, and column three contains lines common to both files.

```
$ comm 1.txt 2.txt
		A
		B
		C
	D
```

The common lines between the two unsorted files can be found with:
```
$ comm -12 <(sort file1.txt) <(sort file2.txt)
```