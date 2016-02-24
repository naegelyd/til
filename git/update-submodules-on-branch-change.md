### Update submodules in Git post checkout hook

Put the following in .git/hooks/post-checkout

```sh
#!/bin/bash

cd ./$(git rev-parse --show-cdup)
git submodule foreach git reset --hard HEAD
git submodule update
```

then, make the post-checkout file executable using:

```sh
chmod +x .git/hooks/post-checkout
```
