# 0x09 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level7@trainer:~$ su - level8
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

Welcome to Level 8

For this level the password is in an executable hidden in one of these sub-directories.  When you run the executable it will print out the flag.  To run the executable type: ./executable

type: man find

After finding and executing the binary, you should try to run the command strings on the it and review the output.  type: strings <executable>

level8@trainer:~$ ls
checklist.chk  dir13  dir18  dir22  dir27  dir31  dir36  dir40  dir45  dir5   dir9
dir1           dir14  dir19  dir23  dir28  dir32  dir37  dir41  dir46  dir50  helpme
dir10          dir15  dir2   dir24  dir29  dir33  dir38  dir42  dir47  dir6   welcome_message
dir11          dir16  dir20  dir25  dir3   dir34  dir39  dir43  dir48  dir7
dir12          dir17  dir21  dir26  dir30  dir35  dir4   dir44  dir49  dir8

level8@trainer:~$ strings checklist.chk
14556e7c704da0db5d7e5ef967fcc5d9  ./welcome_message
1e35339f9660d94cf11f75c5e2753a9f  ./checklist.chk
9afa484b24898f294e70031c369156dc  ./helpme
695cb2c3531973a3204398dac538a6b0  ./.ssh/known_hosts
f2c04e38b770c6e3bd2f797cc93d811f  ./dir24/subdir13/level9_password
22bfb8c1dd94b5f3813a2b25da67463f  ./.bash_logout
ee35a240758f374832e809ae0ea4883a  ./.bashrc
c54f77d63cec0883f3caef6bf05523f0  ./.lesshst
4900e95d4a9cf68d7a87a63325250b62  ./.viminfo
f4e81ade7d6f9fb342541152d08e7a97  ./.profile

level8@trainer:~$ cd dir24/subdir13/

level8@trainer:~/dir24/subdir13$ ls
level9_password

level8@trainer:~/dir24/subdir13$ ./level9_password
The password is: 96ab15e954f1267ea04c35de2d771c2b
```

## Flag

```96ab15e954f1267ea04c35de2d771c2b```
