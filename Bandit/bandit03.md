## Level 3
The password for the next level is stored in a hidden file in the inhere directory.

## Requirements
- cd, ls command, cat

## Solution
```bash
# Move to the directory first
$ cd inhere

# List all files (including hidden ones)
$ ls -la

# Read the hidden file
$ cat .hidden
