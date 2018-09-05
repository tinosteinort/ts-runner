ts-runner
=========

Run TypeScript files directly without (manually) transpiling them to JavaScript.

`ts-runner` requires `nodejs`.


# Preparation

Clone repo and set `ts-runner` executable
```
git clone https://github.com/tinosteinort/ts-runner
cd ts-runner
chmod +x ts-runner
```

## Define the interpreter of the file

`ts-runner` is used as interpreter for the TypeScript file, so it must be
 referenced in the first line of the file. If the target script file is
 in the same directory as the `ts-runner`, it is enough to add
```
#!ts-runner
```
If `ts-runner` is in your home folder you can add
```
#!~/ts-runner
```
If `ts-runner` is on the $PATH you can add
```
#!/usr/bin/env ts-runner
```
... and so on...



# Example

Create file `examplescript.ts` and add the following content:
```
#!ts-runner

const value: string = 'Hello ts-runner';
console.log(value);
```

Set the script file executable:
```
chmod +x examplescript.ts
```

Now, you are able to execute the script. Type in the terminal:
```
./examplescript.ts
```


# Alternatives

There are other tools, that do the same: see `ts-node`