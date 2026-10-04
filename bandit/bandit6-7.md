# Bandit Level 6 → Level 7

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit7.html)

The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size

## Solution

```shell
ssh bandit6@bandit.labs.overthewire.org -p 2220  # (with password 'pXa26xhMWaC2SvDotA4r9EgZkulOeSBW')
cd / && cat $(find . -size 33c -user bandit7 -group bandit6 2>/dev/null)
```

## Result

We've got password `Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3`!
