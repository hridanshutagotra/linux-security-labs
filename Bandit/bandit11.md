## Level 11
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Requirements
- Rot13 - an older encryption method
- tr - translate command used to replace characters with others

## Solution
```bash
$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
