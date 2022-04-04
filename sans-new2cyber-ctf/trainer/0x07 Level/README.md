# 0x07 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level5@trainer:~$ su - level6
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

Welcome to Level 6

The password for the next level is in this user's home directory, however this time there are too many directories to manually dig through.  For this level you will need the find command and search for a file that has pass in the title.

type: man find    read searching for filenames

level6@trainer:~$ find . -name "*password*"
./dir13/subdir40/level7_password
./level6_password

level6@trainer:~$ cat dir13/subdir40/level7_password
The password for level7 is:

RG8geW91IGV2ZW4gbGlmdCBicm8g
```

## Flag

```RG8geW91IGV2ZW4gbGlmdCBicm8g```
