# Writeup "OverTheWire Bandit Level 9 → Level 10"

## Description : 
- The password for the next level is stored in the file data.txt in one of the **few human-readable strings**, preceded by several **=** characters.

## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
  $ ssh bandit9@bandit.labs.overthewire.org -p 2220
```
bandit9@bandit.labs.overthewire.org's password: `UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR`

- we have an idea that's the file is not all human-readable, so i'll use `strings` and we have a hint *** preceded by several **=** characters ***
 I'll use `grep` too
 ```diff
  bandit9@bandit:~$ strings data.txt | grep '='
+  ========== the*2i"4
  =:G e
+  ========== password
  <I=zsGi
+  Z)========== is
  A=|t&E
  Zdb=
  c^ LAh=3G
  *SF=s
+  &========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
  S=A.H&^
 ```
 - And here is the password for the next level `truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk`
