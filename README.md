# yarn-bin-missing

Steps to reproduce:

Step 1: Jest is installed in workspace root and binary is present after running `yarn`

```
> yarn
> ls node_modules/.bin/jest
# node_modules/.bin/jest
```

Step 2: Go to `foo` workspace and install Lodash

```
> cd cd packages/foo
> yarn add lodash
```

Step 3: Go to back to root and 💨 `node_modules/.bin` is gone.

```
> cd -
> ls node_modules/.bin/jest
ls: node_modules/.bin/jest: No such file or directory
```
