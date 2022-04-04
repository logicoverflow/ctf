# 0x10 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level14@trainer:~$ su - level15
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

Welcome to Level 15

For this level you are going to familiarize yourself with the distro version.  We are just looking for the distro name.  example: Fedora 31, then the password would be Fedora

Understanding distro versions can help when searching for exploits with tools like searchsploit or exploitdb (Sorry, there isn't any exploits for this distro, I hope)

type: man hostnamectl
      man lsb_release
      google linux distro

level15@trainer:~$ lsb_release -a
No LSB modules are available.
Distributor ID: Debian
Description:    Debian GNU/Linux 10 (buster)
Release:        10
Codename:       buster

level15@trainer:~$ hostnamectl
   Static hostname: trainer
         Icon name: computer-vm
           Chassis: vm
        Machine ID: 4f7efe5cdd5741dcbc6e4ea27624480c
           Boot ID: 81cbb41b1d704f6eafe2eb025e7fc629
    Virtualization: kvm
  Operating System: Debian GNU/Linux 10 (buster)
            Kernel: Linux 4.19.0-19-cloud-amd64
      Architecture: x86-64
```


## Flag

```Debian```
