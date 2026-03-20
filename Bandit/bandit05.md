## Level 5
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable

## Requirements
- find, ls ,cat

## Solution
```bash
# cd into the inhere directory
$ cd inhere

# we can use the find command with the required flags to narrow down our search
$ find -size 1033c ! -executable
