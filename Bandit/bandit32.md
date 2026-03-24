## Level 32
After all this git stuff, it’s time for another escape. Good luck!

## Requirements:
- $0 : postition parameter

## Theory
So in this level, we're somehow trapped in a 'UPPERCASE SHELL' that just converts any command we give to upper case, and since commands are case sensitive, it will keep giving us error, so we have to find a way to change shells. The one thing in Linux that is uppercase is variables. Specifically, the variable $0 has a reference to a shell. You can see this with echo $0 on your machine. This lets us break out of the uppercase shell and get the password for bandit 33.

## Solution
```bash
>> $0
$ cat /etc/bandit_pass/bandit33
