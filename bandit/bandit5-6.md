# Bandit Level 5 → Level 6

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit6.html)

The password for the next level is stored in a file somewhere under the inhere directory and has
all of the following properties:

human-readable
1033 bytes in size
not executable


## Solution

```shell
ssh bandit5@bandit.labs.overthewire.org -p 2220  # (with password '6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG')
cat $(find -size 1033c)
```

## Result

We've got password `pXa26xhMWaC2SvDotA4r9EgZkulOeSBW`!
