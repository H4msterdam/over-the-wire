# Bandit level 6
Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size
Password for this level: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

### Key Concepts from this level
The key concepts for this level was to learn to find the password file by filterering all results by the paramaters given in the hints of the puzzle intro.
1.filter by filesize (-size sizec)
2.filter by user group (-group nameOfGroup)
1. filter by user (-user nameOfUser)

## Steps

<details>
  <summary>See solution</summary>


  ### Solution

  ```zsh
  bandit6@bandit:~$ ls
bandit6@bandit:~$ cd ..
bandit6@bandit:/home$ cd ..
bandit6@bandit:/$ ls
bin   drifter     home     lib32   lost+found  opt   run   srv  usr
boot  etc         krypton  lib64   media       proc  sbin  sys  var
dev   formulaone  lib      libx32  mnt         root  snap  tmp
bandit6@bandit:/$ find . -size 33c -user bandit6 -group7 2>&1 | grep -v
"Permission"
find: unknown predicate `-group7'
bandit6@bandit:/$ find . -size 33c -user bandit6 -group bandit7 2>&1 | grep -v "Permission"
find: ‘./proc/1792328/task/1792328/fd/6’: No such file or directory
find: ‘./proc/1792328/task/1792328/fdinfo/6’: No such file or directory
find: ‘./proc/1792328/fd/5’: No such file or directory
find: ‘./proc/1792328/fdinfo/5’: No such file or directory
bandit6@bandit:/$ find . -size 33c -user bandit7 -group bandit6 2>&1 | grep -v "Permission"
./var/lib/dpkg/info/bandit7.password
find: ‘./proc/1792766/task/1792766/fd/6’: No such file or directory
find: ‘./proc/1792766/task/1792766/fdinfo/6’: No such file or directory
find: ‘./proc/1792766/fd/5’: No such file or directory
find: ‘./proc/1792766/fdinfo/5’: No such file or directory
bandit6@bandit:/$ cat ./var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:/$


  ```

</details>

