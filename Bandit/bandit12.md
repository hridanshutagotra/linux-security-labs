## Level 12
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level, it may be useful to create a directory under /tmp in which you can work using mkdir.

## Requirements
- mktemp -d: used to create a temporary directory
- cp : copy
- mv : move and rename
- xxd,tar,gzip,bzip2 : compresssion and decompression commands
- file command

## Solution
```bash
$ mktemp -d

# move into the temporary directory
$ cd ./tmp/tmp.X5u51K0

# copy the data file to this directory
$ cp ~/data.txt .

# Rename it to avoid confuison
$ mv data.txt hexdump

# Use file to find the file type
$file hexdump

# It'll show the file type, then from the above commands in the requirements section,
# choose the suitable ones to decompress it, matching with the file type
