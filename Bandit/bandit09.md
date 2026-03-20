## Level 9
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## Requirements
- Strings command
- grep
- pipe command

## Solution
```bash
$ strings data.txt | grep =
