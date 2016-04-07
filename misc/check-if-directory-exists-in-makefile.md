### Check if a directory exists in a Makefile

You can check if a directory exists by using the [wildcard](https://www.gnu.org/software/make/manual/html_node/Wildcard-Function.html) function. Let's look at a simple example where we only want to run a download of a very large directory if it is not already present.

```make
DIR_TO_CHECK_FOR = 'large_directory'

download_data:
    ifeq ("$(wildcard $(DIR_TO_CHECK_FOR))", "")
        @echo "Directory does not exist."
        # Perform download...
    else
        @echo "Skipping download because directory already exists."
    endif
```

This leverages `wildcard` to get back a space-separated list of files that match the supplied pattern, which we set to `$(DIR_TO_CHECK_FOR)` in this case. If the list is empty, then we claim the directory does not exist and we could put our long-running download in there.
