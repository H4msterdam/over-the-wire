# Bandit level 9
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

the Password for this level is: EN632PlfYiZbn3PhVK3XOGSlNInNE00t
### Key Concepts from this level
1. Possible solution is to use strings and sed in conjunction
2. Keyfinding is to remove = and whitespace

## Steps

<details>
  <summary>See solution</summary>


  ### Solution

  ```zsh
bandit9@bandit:~$ cat data.txt | strings -n 20 | sed -r "s/=+//g; s/\s//"
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$
  ```

</details>

