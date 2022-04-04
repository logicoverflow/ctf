# 0x05 Beacons annoying
> 100 (Network)

## Challenge

Connect to ip: 10.112.3.88 port: 7000, a beacon awaits you

author: [@NOPResearcher](https://twitter.com/nopresearcher)

## Solution

Terminal 1
```
┌──(logicoverflow㉿kali)-[~]
└─$ ssh -J tunneler@tunneler.threatsims.com:2222 whistler@10.218.176.199 -L 5000:10.112.3.88:7000
tunneler@tunneler.threatsims.com's password: 
whistler@10.218.176.199's password: 
Welcome to Ubuntu 20.04.4 LTS (GNU/Linux 4.15.0-171-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Sun Mar 27 22:21:32 2022 from 10.218.176.93
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

Terminal 2
```
──(logicoverflow㉿kali)-[~]
└─$ nc -vn 127.0.0.1 5000
(UNKNOWN) [127.0.0.1] 5000 (?) open

I hope you like tunneling, I will send you the flag on a random port... How fast is your tunnel game?
I will send the flag to ip: 10.112.3.199 on port: 12875 in 15 secondsthe flag was sent, I hope you got it!  
```

Terminal 3
```
┌──(logicoverflow㉿kali)-[~]
└─$ ssh -J tunneler@tunneler.threatsims.com:2222 whistler@10.218.176.199 -R 10.112.3.199:12875:127.0.0.1:5500
tunneler@tunneler.threatsims.com's password: 
whistler@10.218.176.199's password: 
Welcome to Ubuntu 20.04.4 LTS (GNU/Linux 4.15.0-171-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Sun Mar 27 22:22:43 2022 from 10.218.176.93
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

Terminal 4
```
┌──(logicoverflow㉿kali)-[~]
└─$ nc -nlvp 5500
listening on [any] 5500 ...
connect to [127.0.0.1] from (UNKNOWN) [127.0.0.1] 50280
ts{YourTunnelGameisAlright}
```

## Flag

```ts{YourTunnelGameisAlright}```
