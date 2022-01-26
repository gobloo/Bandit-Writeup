# Writeup "OverTheWire Bandit Level 7 → Level 8"

## Description : 
- The password for the next level is stored in the file data.txt next to the word millionth
## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
$ ssh bandit7@bandit.labs.overthewire.org -p 2220
```
bandit6@bandit.labs.overthewire.org's password: `HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs`

- Search something inside a file <==> `grep` command
```
bandit7@bandit:~$ grep "millionth" ./data.txt
millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

- And here is the password for the next level `cvX2JJa4CFALtqS87jk27qwqGhBM9plV`
