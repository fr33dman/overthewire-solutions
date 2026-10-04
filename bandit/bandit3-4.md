# Bandit Level 3 → Level 4

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit4.html)

The password for the next level is stored in a hidden file in the inhere directory.

## Solution

```shell
ssh bandit3@bandit.labs.overthewire.org -p 2220  # (with password '7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME')
cat "inhere/...Hiding-From-You"
```

## Result

We've got password `xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq`!
