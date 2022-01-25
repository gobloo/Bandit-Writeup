# Writeup "OverTheWire Bandit Level 0 → Level 1"


## Description : 
- The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Solution :
- First, we need to connect to ssh on port 2220: 
```
$ ssh bandit0@bandit.labs.overthewire.org -p 2220
```
bandit0@bandit.labs.overthewire.org's password:  `bandit0`

- The password is stored in file `readme` located in the home directory 
```
bandit0@bandit:~$ ls
readme
```
- We try to see the content
```
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

