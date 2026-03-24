## Level 22
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

## Requirements
- Cron

## Solution
```bash
$ cat /etc/cron.d/cronjob_bandit23

# The above command will provide us location to a script that we have to decode for the password

$ cat /usr/bin/cronjob_bandit23.sh

# After reading the above script, it should provide us with a command. We substitute `$myname with bandit23 and run it

$ echo I am user bandit23 | md5sum | cut -d ' ' -f 1

# Finally, we cat the output file directory for the password
$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
