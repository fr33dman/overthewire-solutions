# Bandit Level 30 → Level 31

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit31.html)

There is a git repository at ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo 
via the port 2220. The password for the user bandit30-git is the same as for the user bandit30.

From your local machine (not the OverTheWire machine!), clone the repository and find the password 
for the next level. This needs git installed locally on your machine.

## Solution

```shell
cd $(mktemp -d) && git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo && cd repo  # (with password 'jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX')
git tag
git show secret
```

## Result

We've got password `82NkymblpGBYmIXG6ZQ8YldBYstHpfUf`!
