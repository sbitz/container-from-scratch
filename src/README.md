# Build bash

Run 
```shell
docker build -f Containerfile foo/bash .
```

Of course name your image whatever you'd like. Running it will land you in a bash shell, but you won't be able to do anything else because you only have a shell.

```shell
docker run --rm -it foo/bash
```
