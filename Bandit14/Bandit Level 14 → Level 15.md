# Writeup "OverTheWire Bandit Level 14 → Level 15"

## Description : 
-The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.
## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
  $ ssh bandit14@bandit.labs.overthewire.org -p 2220
```
bandit13@bandit.labs.overthewire.org's password: `4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e`

- We need to submit the password of bandit14 to port 30000 on localhost:
```
bandit14@bandit:~$ echo "4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e" | nc localhost 30000
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr

```

- And here is the password for the next level `BfMYroe26WYalil77FoDi9qh59eK5xNr`
