## Level 21
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

# Requirements
- cron
- crontab

## Theory
Cron is like a built-in alarm clock or scheduler used to run commands or scripts at specific times or intervals

## Solution
```bash
# Let's enter the directory cron program is located
$ cd /etc/cron.d

# Check the contents of the directory and read the relevant process file
$ cat cronjob_bandit22

# the cron job script will give you a file that we will read using cat command for the password
$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
