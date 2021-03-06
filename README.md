# Assorted code snippets

### Categories:
 * [Bash](#bash)
 * [Git](#git)
 * [Miscellaneous](#miscellaneous)
 * [Vim](#vim)


### Bash
 * [List files by number of lines](bash/list-files-by-line-count.md)
 * [Recursive find and replace](bash/find-and-replace.md)
 * [Find files in date/time range](bash/find-files-in-date-range.md)

### Docker
 * Remove stopped containers:
  * `docker rm $(docker ps -a -q)`
 * Remove untagged images:
  * `docker rmi $(docker images | grep "^<none>" | awk '{print $3}')`
 * Remove unused images:
  * `docker rmi $(docker images -q)`

### Git
 * [Automatically remove pyc file on branch change](git/delete-pyc-files-on-branch-change.md)
 * [Update submodules on branch change](git/update-submodules-on-branch-change.md)

### Miscellaneous
 * [Check if directory exists in Makefile](misc/check-if-directory-exists-in-makefile.md)

### Vim
 * [Open files listed from command](vim/open-list-of-files-from-command.md)
 * [Sort selected lines](vim/sort-selected-lines.md)
 * [Wrapping text with `gq`](vim/wrapping-with-gq.md)
