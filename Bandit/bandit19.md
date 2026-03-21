## Level 19
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Requiments
- read setuid on wiki or google search

## Solution
```bash
# setuid basically lets a normal user run a program with the power of the file's owner
$ ./bandit20-do cat /etc/bandit_pass/bandit20
