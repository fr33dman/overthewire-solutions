# Bandit Level 29 → Level 30

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit30.html)

There is a git repository at ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo 
via the port 2220. The password for the user bandit29-git is the same as for the user bandit29.

From your local machine (not the OverTheWire machine!), clone the repository and find the password 
for the next level. This needs git installed locally on your machine.

## Solution

```shell
cd $(mktemp -d) && git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo && cd repo  # (with password 'Em7eGtqaMySwNFjCpwzzHhLhospOcdt0')
git branch -a
git fetch --all  # (with password 'Em7eGtqaMySwNFjCpwzzHhLhospOcdt0')
git switch remotes/origin/dev --detach
cat README.md
```

## Result

```text
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX
```

We've got password `jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX`!
