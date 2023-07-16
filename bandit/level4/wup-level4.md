# Bandit level 4
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
### Key Concepts from this levelLevel Goal
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.?
Password for this level:2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
1. The key elements here is find, can you learn to use the -exec {} \;
2. It also worth to know that there is a linux program called strings, check that one out

## Steps

<details>
  <summary>See solution</summary>


  ### Solution

  ```zsh
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ find . -type f -exec cat {} \;
EQ"p
4}]GAu[/9'cwk^jM;,co9??6=>>?w<U'=@ZxjlrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
MrjSr_E,G+h|+
=>KQB?b<Q?+ViO1[5{jmDB0DtQ*)AV ]?lx(z.T26 F8qqlYvFN#'~?3[?N|?G|bG[8y?*

                                                                      2]o-p8q?D
                                                                                .~&?"PTIbandit4@bandit:~/inhere$ find . -type f -exec strings {} \;
cwk^
<U'=
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
=>KQ
.T26
F8qqlY
]o-p8q
bandit4@bandit:~/inhere$ find . -type f -exec strings -n 10 {} \;
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$

  ```

</details>

