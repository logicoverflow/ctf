# 0x08 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level6@trainer:~$ su - level7
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

Welcome to Level 7


The password for the next level is in the password_directory.  For this level though, all files are exactly the same size.  You should look through each file to find the one that contains the password.

Hint: look for password

type: man find
      man grep
      man xargs

level7@trainer:~$ ls
helpme  password_directory  welcome_message

level7@trainer:~$ cd password_directory/

level7@trainer:~/password_directory$ ls
level8_password1    level8_password24  level8_password4   level8_password55  level8_password70  level8_password86
level8_password10   level8_password25  level8_password40  level8_password56  level8_password71  level8_password87
level8_password100  level8_password26  level8_password41  level8_password57  level8_password72  level8_password88
level8_password11   level8_password27  level8_password42  level8_password58  level8_password73  level8_password89
level8_password12   level8_password28  level8_password43  level8_password59  level8_password74  level8_password9
level8_password13   level8_password29  level8_password44  level8_password6   level8_password75  level8_password90
level8_password14   level8_password3   level8_password45  level8_password60  level8_password76  level8_password91
level8_password15   level8_password30  level8_password46  level8_password61  level8_password77  level8_password92
level8_password16   level8_password31  level8_password47  level8_password62  level8_password78  level8_password93
level8_password17   level8_password32  level8_password48  level8_password63  level8_password79  level8_password94
level8_password18   level8_password33  level8_password49  level8_password64  level8_password8   level8_password95
level8_password19   level8_password34  level8_password5   level8_password65  level8_password80  level8_password96
level8_password2    level8_password35  level8_password50  level8_password66  level8_password81  level8_password97
level8_password20   level8_password36  level8_password51  level8_password67  level8_password82  level8_password98
level8_password21   level8_password37  level8_password52  level8_password68  level8_password83  level8_password99
level8_password22   level8_password38  level8_password53  level8_password69  level8_password84  xargs
level8_password23   level8_password39  level8_password54  level8_password7   level8_password85

level7@trainer:~/password_directory$ grep -ri "password" .
./level8_password68:The password for level8 is:

level7@trainer:~/password_directory$ cat level8_password68
The password for level8 is:

bGV0J3MgZmluZCBzb21ldGhpbmcg
```

## Flag

```bGV0J3MgZmluZCBzb21ldGhpbmcg```
