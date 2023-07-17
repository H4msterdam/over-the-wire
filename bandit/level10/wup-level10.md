# Bandit level 10
The password for the next level is stored in the file data.txt can you encrypt it?

the Password for this level is: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
### Key Concepts from this level
1. Base 64
1.2
## Steps

<details>
  <summary>See solution</summary>


  ### Solution

  ```zsh
  data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ cat data.txt | base64 -d | awk '{print $4}'
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$

  ```

</details>

