# Bandit Level 3
Password for this levLevel Goal
The password for the next level is stored in a hidden file in the inhere directory
Password for this level: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
### Key Concepts from this level?
1. Ls command has some usefull flags, can you use them to find the flag?
2. hidden files on POSIX systems have a symbol for prefix

## Steps

<details>
  <summary>See solution</summary>


  ### Solution

  ```zsh
  bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Apr 23 18:04 .
drwxr-xr-x 3 root    root    4096 Apr 23 18:04 ..
-rw-r----- 1 bandit4 bandit3   33 Apr 23 18:04 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$


  ```

</details>

