# Bandit Level 8 → Level 9

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit9.html)

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Solution

```shell
ssh bandit8@bandit.labs.overthewire.org -p 2220  # (with password 'VR1ljMayciFxbnUokuQmJFw6QC9VKtub')
sort data.txt | uniq -u
```

## Result

We've got password `EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl`!
