# Writeup "OverTheWire Bandit Level 1 → Level 2"

## Description : 
- The password for the next level is stored in a file called - located in the home directory

## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
$ ssh bandit1@bandit.labs.overthewire.org -p 2220
```

bandit1@bandit.labs.overthewire.org's password:  `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`

- The password is stored in file `-` located in the home directory 
```
bandit1@bandit:~$ ls
-
```
- We try to see the content
```
bandit1@bandit:~$ cat - 

```
- Nothing happend because it's a hyphen so we should use the command : 
```
bandit1@bandit:~$ cat ./- 
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```
- And here is the password for the next level `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`

