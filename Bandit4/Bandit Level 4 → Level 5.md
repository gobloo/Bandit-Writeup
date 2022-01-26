# Writeup "OverTheWire Bandit Level 3 → Level 4"

## Description : 
- The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
$ ssh bandit4@bandit.labs.overthewire.org -p 2220
```
bandit3@bandit.labs.overthewire.org's password: `pIwrPrtPN36QITSp3EQaw936yaFoFgAB`

- The password is stored in the only human-readable file in the inhere directory
```
  bandit4@bandit:~$ ls
  inhere
  bandit4@bandit:~$ cd inhere
  bandit4@bandit:~/inhere$ ls
  -file00  -file02  -file04  -file06  -file08
  -file01  -file03  -file05  -file07  -file09
```
- Now, we need to find which file contains the password but without try them all so  let's try `file`
```
  bandit4@bandit:~/inhere$ file ./*
  ./-file00: data
  ./-file01: data
  ./-file02: data
  ./-file03: data
  ./-file04: data
  ./-file05: data
  ./-file06: data
  ./-file07: ASCII text
  ./-file08: data
  ./-file09: data
```
- The file we look for is `-file07`
```
  bandit4@bandit:~/inhere$ cat ./-file07
  koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```
- And here is the password for the next level `koReBOKuIDDepwhWk7jZC0RTdopnAYKh`
