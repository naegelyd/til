### Open List of Files From Command

It is trivial to open multiple files in vim using something like `vim file1.txt file2.txt`. That will open each file for editing. Sometimes though, the file list needs to be generated dynamically. For that, we can pass a file list to vim using:

```sh
vim `<command`>`
```

The above will open each of the files listed in the output of `<command>` in a separate buffer. From there, edit, close, and move around buffers as you normally would. For example, let's open all the files in directory `dir1`:

```sh
vim `find dir1 -type f`
```

Or, open all the modified files as reported by git:

```sh
vim `git ls-files --modified`
```
