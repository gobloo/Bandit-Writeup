# Writeup "OverTheWire Bandit Level 3 → Level 4"

## Description : 
- The password for the next level is stored in a hidden file in the inhere directory.
## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
$ ssh bandit3@bandit.labs.overthewire.org -p 2220
```
bandit2@bandit.labs.overthewire.org's password: `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`

- The password is stored in a hidden file in inhere directory 
```
  bandit3@bandit:~$ ls
  inhere
  bandit3@bandit:~$ cd inhere 
  bandit3@bandit:~/inhere$ ls
  bandit3@bandit:~/inhere$ 
```
- We can't see them hidden files with simple ls so we add the attribute `-a`
```c
 bandit3@bandit:~/inhere$ ls -a
 .  ..  .hidden
 bandit3@bandit:~/inhere$ cat .hidden
 pIwrPrtPN36QITSp3EQaw936yaFoFgAB
 ```

- And here is the password for the next level `pIwrPrtPN36QITSp3EQaw936yaFoFgAB`
