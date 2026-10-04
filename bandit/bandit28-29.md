# Bandit Level 28 → Level 29

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit29.html)

There is a git repository at ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo 
via the port 2220. The password for the user bandit28-git is the same as for the user bandit28.

From your local machine (not the OverTheWire machine!), clone the repository and find the password 
for the next level. This needs git installed locally on your machine.

## Solution

```shell
cd $(mktemp -d) && git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo && cd repo  # (with password 'y8Yd2ssKcpHpud7UvOSOxwamRMzIGIeQ')
git log
git checkout fac3dcdd94f71fb2d3286d6531d4b8523ec64d30 && cat README.md
```

## Result

```text
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: Em7eGtqaMySwNFjCpwzzHhLhospOcdt0
```

We've got password `Em7eGtqaMySwNFjCpwzzHhLhospOcdt0`!
