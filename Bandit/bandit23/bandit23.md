## Level 23
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.
Note: This level will serve as introduction to writing bash shell-scripts

## Requirements
- chmod, cron, bash scripting

## Theory
This level requires you to create your own first shell-script. You'll have to again, check the cron process script. The script you'll find basically executes and deletes all the files in a specified folder. For this level, we need to create a script that will give us the password for bandit24 by preventing the early deletion of the password file.
I will be providing the script file in the same folder alongside this md file.

## Solution
```bash
$ cat /etc/cron.d/cronjob_bandit24
$ cat /usr/bin/cronjob_bandit24.sh

# Make a temporary directory
$ mktemp -d

# cd into it
$ cd /tmp/tmp.2tIuL5kV1f

# Create a shell script to take over the running cron activity and get the pass file
# script file in available in the bandit23 directory where you're reading this solution

# give your script file the necessary permissions to run
$ chmod +rx bandit24_pass.sh

# create a file that the script will copy the password to
$ touch password
$ chmod 666 password

# finally, copy your script to the same directory as the directory with the cron script
$ cp bandit24_pass.sh /var/spool/bandit24/

# Now just wait for a minute and then read the password file that you created for the password
$ cat password


