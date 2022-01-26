# Writeup "OverTheWire Bandit Level 2 → Level 3"

## Description : 
- The password for the next level is stored in a file called spaces in this filename located in the home directory
## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
  $ ssh bandit2@bandit.labs.overthewire.org -p 2220
```
bandit2@bandit.labs.overthewire.org's password: `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`
- The password is stored in file `spaces in this filename` located in the home directory 
```
  bandit2@bandit:~$ ls
  spaces in this filename
```
- We try to see the content
```diff
  bandit2@bandit:~$ cat "spaces in this filename"
+  UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```
- And here is the password for the next level `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`
