# Bandit Level 9 → Level 10

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit10.html)

The password for the next level is stored in the file data.txt in one of the few human-readable
strings, preceded by several ‘=’ characters.

## Solution

```shell
ssh bandit9@bandit.labs.overthewire.org -p 2220  # (with password 'EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl')
strings data.txt | grep -E '^=+'
```

## Result

```text
=mTf
========== password
========== is
========== B0s2khmbT9u0geKuOoVGW3JZKhndE3BG
=YqO
=[xi
```

We've got password `B0s2khmbT9u0geKuOoVGW3JZKhndE3BG`!
