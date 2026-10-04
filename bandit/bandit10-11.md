# Bandit Level 10 → Level 11

The password for the next level is stored in the file data.txt, which contains base64 encoded data

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit11.html)


## Solution

```shell
ssh bandit10@bandit.labs.overthewire.org -p 2220  # (with password 'B0s2khmbT9u0geKuOoVGW3JZKhndE3BG')
cat data.txt  | base64 -d
```

## Result

```text
The password is pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro
```

We've got password `pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro`!
