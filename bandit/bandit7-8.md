# Bandit Level 7 → Level 8

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit8.html)

The password for the next level is stored in the file data.txt next to the word millionth

## Solution

```shell
ssh bandit7@bandit.labs.overthewire.org -p 2220  # (with password 'Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3')
cat ./data.txt | grep "millionth"
```

## Result

```text
millionth	VR1ljMayciFxbnUokuQmJFw6QC9VKtub
```

We've got password `VR1ljMayciFxbnUokuQmJFw6QC9VKtub`!
