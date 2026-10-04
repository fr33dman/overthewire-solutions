# Bandit Level 19 → Level 20

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit20.html)

To gain access to the next level, you should use the setuid binary in the homedirectory. 
Execute it without arguments to find out how to use it. The password for this level can be found 
in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Solution

```shell
ssh bandit19@bandit.labs.overthewire.org -p 2220  # (with password 'KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI')
./bandit20-do --chdir /etc/bandit_pass/ cat bandit20
```

## Result

We've got password `4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA`!
