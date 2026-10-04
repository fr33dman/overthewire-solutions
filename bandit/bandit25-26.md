# Bandit Level 25 → Level 26

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit26.html)

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not 
/bin/bash, but something else. Find out what it is, how it works and how to break out of it.

NOTE: if you’re a Windows user and typically use Powershell to ssh into bandit: Powershell is 
known to cause issues with the intended solution to this level. You should use command prompt instead.

## Solution

```shell
scp -P 2220 bandit25@bandit.labs.overthewire.org:~/bandit26.sshkey /tmp/bandit26 && chmod 700 /tmp/bandit26  # (with password 'SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P')
```

We've got the key!

Reduce the terminal window height to just a few lines before connecting, so the text does not 
fit on one screen and `more` pauses instead of exiting. Then press `v` inside `more` to open Vim.

```shell
ssh -p 2220 -i /tmp/bandit26 bandit26@bandit.labs.overthewire.org
v
:set shell=/bin/bash
:shell
cat /etc/bandit_pass/bandit26
```

## Result

We've got password `jHdv2ELQhT22BkprMNDjybZDAkw1zeBJ`!
