### Find and list files by number of lines

The example below will find all CoffeeScript files and present a sorted list descending by line count in the file. Each line in the output will include line count and file name.

```sh
find . -type f -name *.coffee -exec wc -l {} + | sort -rn
```
