# 0x0A Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level8@trainer:~/dir24/subdir13$ su - level9
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

Welcome to Level 9

First a bit of history.  RockYou was a social media site that suffered a security breach in 2009, losing 32 million passwords.  They were storing all the user credentials in plain text in their database.  At the time this was the largest breach of passwords and allowed for academic research and password analysis with real data.  These passwords were eventually organized into a password list that is commonly used for cracking passwords.

For this level we want to find the line number in the rock you wordlist where the password "evilhacker" is found.  That line number is the password for level 10.  The wordlist can be found at /usr/share/wordlists/rockyou.txt (it's in the same place on kali too) Grep uses a 1-based numbering system meaning the first line is 1 and not 0.

type: man grep

level9@trainer:~$ ls
helpme  welcome_message

level9@trainer:~$ grep -in "evilhacker" /usr/share/wordlists/rockyou.txt
955830:evilhacker

```

## Flag

```955830```
