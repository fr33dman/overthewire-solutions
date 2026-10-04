# Bandit Level 11 → Level 12

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit12.html)

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and
uppercase (A-Z) letters have been rotated by 13 positions

## Solution

```shell
ssh bandit11@bandit.labs.overthewire.org -p 2220  # (with password 'pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro')
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

## Result

```text
The password is GROozWPO8QyN0mGrjUkID0WCYkZiQxrN
```

We've got password `GROozWPO8QyN0mGrjUkID0WCYkZiQxrN`!
