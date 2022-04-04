# 0x11 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level15@trainer:~$ su - level16
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

Welcome to Level 16

For this level you are going to familiarize yourself with the aliases.  They can be very useful and can be used for a variety of actions to speed up your workflow.  They can also be very dangerous.

type: google alias

level16@trainer:~$ alias
alias bc='bc -l'
alias devbox='sshpass -p 6b39034a8045ed996a436f8d09031522 ssh level17@trainer.threatsims.com'
alias grep='grep --color=auto'
alias ls='ls --color=auto'
alias mkdir='mkdir -pv'

level16@trainer:~$ cat .bashrc | grep alias
# enable color support of ls and also add handy aliases
    alias ls='ls --color=auto'
    #alias dir='dir --color=auto'
    #alias vdir='vdir --color=auto'
    #alias grep='grep --color=auto'
    #alias fgrep='fgrep --color=auto'
    #alias egrep='egrep --color=auto'
# some more ls aliases
#alias ll='ls -l'
#alias la='ls -A'
#alias l='ls -CF'
# ~/.bash_aliases, instead of adding them here directly.
if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
alias devbox='sshpass -p 6b39034a8045ed996a436f8d09031522 ssh level17@trainer.threatsims.com'
alias grep='grep --color=auto'
alias bc='bc -l'
alias mkdir='mkdir -pv'
```

## Flag

```6b39034a8045ed996a436f8d09031522```
