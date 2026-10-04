# Bandit Level 22 → Level 23

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit23.html)

A program is running automatically at regular intervals from cron, the time-based job scheduler. 
Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. 
The script for this level is intentionally made easy to read. If you are having problems 
understanding what it does, try executing it to see the debug information it prints.

## Solution

```shell
ssh bandit22@bandit.labs.overthewire.org -p 2220  # (with password 'RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz')
cat /etc/cron.d/cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
cat /tmp/$(echo "I am user bandit23" | md5sum | cut -d ' ' -f 1)
```

## Result

We've got password `gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw`!
