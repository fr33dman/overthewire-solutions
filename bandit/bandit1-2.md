# Bandit Level 1 → Level 2

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit2.html)

The password for the next level is stored in a file called - located in the home directory

## Solution

```shell
ssh bandit1@bandit.labs.overthewire.org -p 2220  # (with password '6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR')
cat "./-"
```

## Result

We've got password `PK8fYLZg2hnHSz83plBL1iEPKdD3QToB`!
