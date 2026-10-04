# Bandit Level 2 → Level 3

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit3.html)

The password for the next level is stored in a file called --spaces in this filename-- located in the home directory

## Solution

```shell
ssh bandit2@bandit.labs.overthewire.org -p 2220  # (with password 'PK8fYLZg2hnHSz83plBL1iEPKdD3QToB')
cat "./--spaces in this filename--"
```

## Result

We've got password `7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME`!
