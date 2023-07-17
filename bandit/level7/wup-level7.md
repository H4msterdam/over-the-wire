# Bandit level 7
Level Goal
Bandit Level 7 → Level 8
Level Goal
The password for the next level is stored in the file data.txt next to the word millionth
Password for this level: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

### Key Concepts from this level
The key here is the millionth how can we find it? Maybe grep is your friend?
1. Use grep (dont be lazy)

## Steps

<details>
  <summary>See solution</summary>


  ### Solution

  ```zsh
  bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | grep millionth
millionth	TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ cat data.txt | grep millionth | awk '{print $2}'
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$

  ```

</details>

