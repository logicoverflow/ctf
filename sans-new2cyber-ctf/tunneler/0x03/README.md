# 0x03 SSH in tunnels
> 50 (Network)

## Challenge

SSH through the bastion to the pivot.

IP: 10.218.176.199

User: whistler

Pass: cocktailparty

author: [@NOPResearcher](https://twitter.com/nopresearcher)

## Solution

```
┌──(logicoverflow㉿kali)-[~]
└─$ ssh -J tunneler@tunneler.threatsims.com:2222 whistler@10.218.176.199
tunneler@tunneler.threatsims.com's password: 
The authenticity of host '10.218.176.199 (<no hostip for proxy command>)' can't be established.
ED25519 key fingerprint is SHA256:5/mZmMUFiQg15f/JfPD47eHAo9sYzmati7d/DuJjWIo.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.218.176.199' (ED25519) to the list of known hosts.
whistler@10.218.176.199's password: 
Welcome to Ubuntu 20.04.4 LTS (GNU/Linux 4.15.0-171-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Sat Mar 26 18:00:17 2022 from 10.218.176.93
.___________. __    __  .__   __. .__   __.  _______  __       _______ .______      
|           ||  |  |  | |  \ |  | |  \ |  | |   ____||  |     |   ____||   _  \     
`---|  |----`|  |  |  | |   \|  | |   \|  | |  |__   |  |     |  |__   |  |_)  |    
    |  |     |  |  |  | |  . `  | |  . `  | |   __|  |  |     |   __|  |      /     
    |  |     |  `--'  | |  |\   | |  |\   | |  |____ |  `----.|  |____ |  |\  \----.
    |__|      \______/  |__| \__| |__| \__| |_______||_______||_______|| _| `._____|
                                                                                    
ts{IThoughtWeLostYouOnTheWay}

Pivot-1:

Some things you can do:

Something is Beaconing to the pivot on port 58671-58680 to ip 10.112.3.199, can you tunnel it back?

scan for the ftp server: 10.112.3.207 user: bishop pass: geese  (Its not where you think it is, also the banner is important)

connect to pivot-2 ip: 10.112.3.12 ssh port: 22 user: crease pass: NoThatsaV

connect to ip: 10.112.3.88 port: 7000, a beacon awaits you
```

## Flag

```ts{IThoughtWeLostYouOnTheWay}```
