# Bandit Level 15 → Level 16

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit16.html)

The password for the next level can be retrieved by submitting the password of the current level 
to port 30001 on localhost using SSL/TLS encryption.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” 
section in the manpage.

## Solution

```shell
ssh bandit15@bandit.labs.overthewire.org -p 2220  # (with password 'pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7')
openssl s_client -connect localhost:30001 -ign_eof  # (enter password 'pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7')
```

## Result

```text
Correct!
kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V
```

We've got password `kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V`!
