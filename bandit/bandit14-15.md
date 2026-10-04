# Bandit Level 14 → Level 15

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit15.html)

The password for the next level can be retrieved by submitting the password of the current level 
to port 30000 on localhost.

## Solution

```shell
ssh bandit14@bandit.labs.overthewire.org -p 2220  # (with password 'aaWecNkG4FhxJQxz07uiwzVP6bJiYS65')
cat /etc/bandit_pass/bandit14 | nc localhost 30000
```

## Result

```text
Correct!
pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7
```

We've got password `pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7`!
