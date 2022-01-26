# Writeup "OverTheWire Bandit Level 10 → Level 11"

## Description : 
- The password for the next level is stored in the file data.txt, which contains base64 encoded data
## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
  $ ssh bandit10@bandit.labs.overthewire.org -p 2220
```
bandit10@bandit.labs.overthewire.org's password: `truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk`

- Let's check the file's content
```
  bandit10@bandit:~$ cat data.txt
  VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==
```

- We can use [CYBER CHEF](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true)) , I prefer to use the command line:
```
bandit10@bandit:~$ base64 -d data.txt
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```
- And here is the password for the next level `IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR`
