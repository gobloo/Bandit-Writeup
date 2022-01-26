# Writeup "OverTheWire Bandit Level 8 → Level 9"

## Description : 
- The password for the next level is stored in the file data.txt and is the **only line** of text that **occurs only once**.

## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
  $ ssh bandit8@bandit.labs.overthewire.org -p 2220
```
bandit8@bandit.labs.overthewire.org's password: `cvX2JJa4CFALtqS87jk27qwqGhBM9plV`

- like we see in the question one line and occurs only once, that's mean we will use `uniq` which filters out the repeated lines in a file with the attribute `-u` for uniq line
but there's a probleme uniq : detects the adjacent duplicate lines so lets sort the file first 
```
  bandit8@bandit:~$ sort data.txt | uniq -u
  UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

```
- And here is the password for the next level `UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR`

