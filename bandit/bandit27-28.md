# Bandit Level 27 → Level 28

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit28.html)

There is a git repository at ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo 
via the port 2220. The password for the user bandit27-git is the same as for the user bandit27.

From your local machine (not the OverTheWire machine!), clone the repository and find the password 
for the next level. This needs git installed locally on your machine.

## Solution

```shell
cd $(mktemp -d) && git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo && cd repo  # (with password 'STJLJBRRphMxKB392CT4iOr5CbzPU9ER')
cat README
```

## Result

```text
The password to the next level is: y8Yd2ssKcpHpud7UvOSOxwamRMzIGIeQ
```

We've got password `y8Yd2ssKcpHpud7UvOSOxwamRMzIGIeQ`!
