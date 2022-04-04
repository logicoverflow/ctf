# 0x0B Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level9@trainer:~$ su - level10
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

Welcome to Level 10

For this level you are given a log file from the program fail2ban.  Fail2ban is used monitor log files for suspicious activity like too many failed logins.  It is commonly deployed for use with Apache or SSH.  After a configured number of attempts it will create an iptables (linux firewall) rule to block the ip from communicating with the device for a period of time.

The log file is located in your home directory and is called fail2ban.log.  The password to level 11 is the number of times 112.85.42.94 was banned.

type: man grep
      man wc
      
level10@trainer:~$ head -n 25 fail2ban.log
2019-11-29 18:08:28,460 fail2ban.server         [10950]: INFO    --------------------------------------------------
2019-11-29 18:08:28,460 fail2ban.server         [10950]: INFO    Starting Fail2ban v0.10.2
2019-11-29 18:08:28,466 fail2ban.database       [10950]: INFO    Connected to fail2ban persistent database '/var/lib/fail2ban/fail2ban.sqlite3'
2019-11-29 18:08:28,468 fail2ban.jail           [10950]: INFO    Creating new jail 'sshd'
2019-11-29 18:08:28,488 fail2ban.jail           [10950]: INFO    Jail 'sshd' uses pyinotify {}
2019-11-29 18:08:28,492 fail2ban.jail           [10950]: INFO    Initiated 'pyinotify' backend
2019-11-29 18:08:28,493 fail2ban.filter         [10950]: INFO      maxLines: 1
2019-11-29 18:08:28,512 fail2ban.server         [10950]: INFO    Jail sshd is not a JournalFilter instance
2019-11-29 18:08:28,512 fail2ban.filter         [10950]: INFO    Added logfile: '/var/log/auth.log' (pos = 6678, hash = e00851e7f7b891dedb8d3243544192be8c9f2b55)
2019-11-29 18:08:28,513 fail2ban.filter         [10950]: INFO      encoding: UTF-8
2019-11-29 18:08:28,513 fail2ban.filter         [10950]: INFO      maxRetry: 4
2019-11-29 18:08:28,513 fail2ban.filter         [10950]: INFO      findtime: 600
2019-11-29 18:08:28,514 fail2ban.actions        [10950]: INFO      banTime: 60
2019-11-29 18:08:28,516 fail2ban.jail           [10950]: INFO    Jail 'sshd' started
2019-11-29 18:44:52,739 fail2ban.filter         [10950]: INFO    [sshd] Found 144.202.34.43 - 2019-11-29 18:44:52
2019-11-29 18:44:52,749 fail2ban.filter         [10950]: INFO    [sshd] Found 144.202.34.43 - 2019-11-29 18:44:52
2019-11-29 18:44:55,454 fail2ban.filter         [10950]: INFO    [sshd] Found 144.202.34.43 - 2019-11-29 18:44:55
2019-11-29 18:58:49,715 fail2ban.filter         [10950]: INFO    [sshd] Found 144.202.34.43 - 2019-11-29 18:58:49
2019-11-29 18:58:49,716 fail2ban.filter         [10950]: INFO    [sshd] Found 144.202.34.43 - 2019-11-29 18:58:49
2019-11-29 18:58:51,475 fail2ban.filter         [10950]: INFO    [sshd] Found 144.202.34.43 - 2019-11-29 18:58:51
2019-11-29 19:01:43,988 fail2ban.filter         [10950]: INFO    [sshd] Found 144.202.34.43 - 2019-11-29 19:01:43
2019-11-29 19:01:44,362 fail2ban.actions        [10950]: NOTICE  [sshd] Ban 144.202.34.43
2019-11-29 19:01:46,696 fail2ban.filter         [10950]: INFO    [sshd] Found 144.202.34.43 - 2019-11-29 19:01:46
2019-11-29 19:02:44,539 fail2ban.actions        [10950]: NOTICE  [sshd] Unban 144.202.34.43
2019-11-29 19:05:13,989 fail2ban.filter         [10950]: INFO    [sshd] Found 144.202.34.43 - 2019-11-29 19:05:13

level10@trainer:~$ grep "Ban 112.85.42.94" fail2ban.log > banned.txt

level10@trainer:~$ wc -l banned.txt
192 banned.txt
```

## Flag

```192```
