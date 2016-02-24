### Delete .pyc files in Git post checkout hook

Put the following in .git/hooks/post-checkout

```sh
#!/bin/bash

cd ./$(git rev-parse --show-cdup)
find . -name "*.pyc" -delete
```

then, make the post-checkout file executable using:

```sh
chmod +x .git/hooks/post-checkout
```
