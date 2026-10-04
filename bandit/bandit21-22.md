# Bandit Level 21 → Level 22

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit22.html)

A program is running automatically at regular intervals from cron, the time-based job scheduler. 
Look in /etc/cron.d/ for the configuration and see what command is being executed.

## Solution

```shell
ssh bandit21@bandit.labs.overthewire.org -p 2220  # (with password 'bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY')
ls /etc/cron.d/
cat /etc/cron.d/cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

## Result

We've got password `RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz`!
