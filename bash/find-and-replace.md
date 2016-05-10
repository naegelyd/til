### Find and replace in files

The below will search all files in the current directory for the string `old` and replace it with the string `new`.

```sh
perl -p -i -e "s/old/new/g" *
```

To do the search and replace recursively, something like the following will work.

```sh
find . -name "*.py" -print0 | xargs -0 perl -p -i -e "s/old/new/g"
```

Or for files matching some grep query

```sh
grep -ril some_search_string . | xargs perl -p -i -e "s/old/new/g"
```

`perl` options:
 * `-i` Edit files in place
 * `-e` Line of a program to be run
 * `-p` Loop over program and print line, like `sed`
