## Level 4
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

## Requirements
- file command

## Solution
```bash
# cd into the inhere directory
$ cd inhere

# use the file command to check the file types
$ file ./*

# use the cat command to read the only ascii text file
$ cat ./-file07
