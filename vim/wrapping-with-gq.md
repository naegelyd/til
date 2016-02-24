### Formatting/Wrapping text with `gq`

You can format/wrap text using the `gq{motion}` command. For example, `gqq` will format the current line. `gqip` will format the current paragraph. `{Visual}gq` will format the selection.

Example use case. Imagine you type a long line comment but want to wrap to keep within line length of 80(or whatever textwidth is). Given the following example of a comment in a python file:

```python
# Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

you could put the cursor on the line and run `gqq` to get the following(leading `#` included during the wrapping process):

```python
# Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
# tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
# quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
# consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
# cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
# proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```


More info [in the docs](http://vimdoc.sourceforge.net/htmldoc/change.html#formatting).
