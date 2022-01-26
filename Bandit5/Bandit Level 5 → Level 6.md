# Writeup "OverTheWire Bandit Level 4 → Level 5"

## Description : 
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

  - human-readable
  - 1033 bytes in size : 1byte = 1 character 
  - not executable

## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
$ ssh bandit5@bandit.labs.overthewire.org -p 2220
```
bandit5@bandit.labs.overthewire.org's password: `koReBOKuIDDepwhWk7jZC0RTdopnAYKh`

- We need to look for a file, the first thing in our mind is using `find` command 

```
  bandit5@bandit:~$ cd inhere
  bandit5@bandit:~/inhere$ find . -size 1033c ! -executable
  ./maybehere07/.file2
```

- Let's see this file's content 
```
  bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
  DXjZPULLxYr17uwoI01bNLQbtFemEgo7

```
- And here is the password for the next level `DXjZPULLxYr17uwoI01bNLQbtFemEgo7`


