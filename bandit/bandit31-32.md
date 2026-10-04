# Bandit Level 31 → Level 32

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit32.html)

There is a git repository at ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo 
via the port 2220. The password for the user bandit31-git is the same as for the user bandit31.

From your local machine (not the OverTheWire machine!), clone the repository and find the password 
for the next level. This needs git installed locally on your machine.

## Solution

```shell
cd $(mktemp -d) && git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo && cd repo  # (with password '82NkymblpGBYmIXG6ZQ8YldBYstHpfUf')
echo "" > .gitignore && echo "May I come in?" > key.txt && git add . && git commit -m "give me pass" && git push  # (with password '82NkymblpGBYmIXG6ZQ8YldBYstHpfUf')
```

## Result

```text
.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.

Well done! Here is the password for the next level:
pWuj5jBQ6IgV0NXwiH6g1pXRF8S1YvbT

.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
```

We've got password `pWuj5jBQ6IgV0NXwiH6g1pXRF8S1YvbT`!
