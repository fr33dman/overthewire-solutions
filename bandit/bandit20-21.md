# Bandit Level 20 → Level 21

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit21.html)

There is a setuid binary in the homedirectory that does the following: it makes a connection to 
localhost on the port you specify as a commandline argument. It then reads a line of text from 
the connection and compares it to the password in the previous level (bandit20). 
If the password is correct, it will transmit the password for the next level (bandit21).

## Solution

```shell
ssh bandit20@bandit.labs.overthewire.org -p 2220  # (with password '4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA')
printf "4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA" | nc -v -l localhost 12345 &
./suconnect 12345
```

## Result

```text
Connection received on localhost 44140
Read: 4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA
Password matches, sending next password
bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY
```

We've got password `bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY`!
