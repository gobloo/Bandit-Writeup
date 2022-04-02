# Writeup "OverTheWire Bandit Level 11 → Level 12"

## Description : 
- The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Solution :
- First, we need to connect to ssh on port 2220 and we use the password founded in the previous level: 
```
  $ ssh bandit11@bandit.labs.overthewire.org -p 2220
```
bandit11@bandit.labs.overthewire.org's password: `IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR`

- Let's check the file's content
```
  bandit10@bandit:~$ cat data.txt
  Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh
```

- We can use [CYBER CHEF](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)) , I prefer to use the command line:
```
bandit11@bandit:~$ alias Rot13="tr 'A-Za-z' 'N-ZA-Mn-za-m'"
bandit11@bandit:~$ cat data.txt | ROT13
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```
- And here is the password for the next level `5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu`
