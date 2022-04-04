# 0x06 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level4@trainer:~$ su - level5
Password:

    ====================================================================
    ||                                                                ||
    ||     .--.          Welcom to the Linux Trainer!                 ||
    ||    | o_o|                                                      ||
    ||    | ==>|          To view the level instructions again        ||
    ||   / /   \ \         type: cat welcome_message                  ||
    ||  ( |     | )                                                   ||
    || /' |_____/'\       Getting Stuck? Need help with a level?      ||
    || \___)--(___/         type:  cat helpme                         ||
    ||                                                                ||
    ||                    Use "su - level#"  to change levels         ||
    ||                                                                ||
    ||                    feedback: nopresearcher@gmail.com           ||
    ||                                                                ||
    ||                                                                ||
    ====================================================================

Welcome to Level 5

For this level the password is in level6's home directory.  Due to a persmissions error, the level5 user can access it.  Think about the directories you have already seen and what file name patterns.

level5@trainer:~$ ls
helpme  welcome_message

level5@trainer:~$ cd ..

level5@trainer:/home$ ls
level0  level10  level12  level14  level16  level18  level2   level21  level3  level5  level7  level9
level1  level11  level13  level15  level17  level19  level20  level22  level4  level6  level8  trainer

level5@trainer:/home$ cd level6

level5@trainer:/home/level6$ ls
dir1   dir14  dir19  dir23  dir28  dir32  dir37  dir41  dir46  dir50  helpme
dir10  dir15  dir2   dir24  dir29  dir33  dir38  dir42  dir47  dir6   level6_password
dir11  dir16  dir20  dir25  dir3   dir34  dir39  dir43  dir48  dir7   welcome_message
dir12  dir17  dir21  dir26  dir30  dir35  dir4   dir44  dir49  dir8
dir13  dir18  dir22  dir27  dir31  dir36  dir40  dir45  dir5   dir9

level5@trainer:/home/level6$ cat level6_password
7cb1963d316b9a302cf6c204d35b7302
```

## Flag

```7cb1963d316b9a302cf6c204d35b7302```
