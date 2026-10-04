# Bandit Level 18 → Level 19

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit19.html)

The password for the next level is stored in a file readme in the homedirectory. 
Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## Solution

```shell
ssh bandit18@bandit.labs.overthewire.org -p 2220 'cat readme'  # (with password 'OQxXZjELndr90zuhOTDYBEomI0SZITXI')
```

## Result

We've got password `KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI`!
