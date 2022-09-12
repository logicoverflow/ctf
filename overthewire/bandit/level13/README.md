# Level 13

## Challenge

The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

Reference: [Bandit Level 13](https://overthewire.org/wargames/bandit/bandit13.html)

#### Commands you may need to solve this level

```grep```, ```sort```, ```uniq```, ```strings```, ```base64```, ```tr```, ```tar```, ```gzip```, ```bzip2```, ```xxd```, ```mkdir```, ```cp```, ```mv```, ```file```

## Solution

```
┌──(logicoverflow㉿RZR-LP)-[~]
└─$ ./bandit.sh 12
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit12@bandit.labs.overthewire.org's password:

      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

 Both python2 and python3 are installed.

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ cd /tmp/
bandit12@bandit:/tmp$ mkdir bt12
bandit12@bandit:/tmp$ cd bt12
bandit12@bandit:/tmp/bt12$ cp ~/data.txt .
bandit12@bandit:/tmp/bt12$ ls
data.txt
bandit12@bandit:/tmp/bt12$ head data.txt
00000000: 1f8b 0808 7151 1063 0203 6461 7461 322e  ....qQ.c..data2.
00000010: 6269 6e00 013f 02c0 fd42 5a68 3931 4159  bin..?...BZh91AY
00000020: 2653 595d ed11 a800 001b ffff d8ff fde7  &SY]............
00000030: dff7 ffff ffcf efcf bef7 7e7f dd39 3f7f  ..........~..9?.
00000040: fafb ffbf cfbf 3eff a9fb bf7f b001 3b1b  ......>.......;.
00000050: 6d20 0f50 0034 0680 0000 34c2 01ea 0d34  m .P.4....4....4
00000060: 0000 1900 1a32 1a68 0d00 0000 0034 0000  .....2.h.....4..
00000070: 000d 0069 91ea 0c6d 5100 0068 00c8 000d  ...i...mQ..h....
00000080: 0323 4340 3d40 0d0d 1a68 01a3 4c83 401a  .#C@=@...h..L.@.
00000090: 687a 4034 0340 1a00 3468 0188 c868 34d0  hz@4.@..4h...h4.
bandit12@bandit:/tmp/bt12$ xxd -r data.txt > data
bandit12@bandit:/tmp/bt12$ ls
data  data.txt
bandit12@bandit:/tmp/bt12$ file data
data: gzip compressed data, was "data2.bin", last modified: Thu Sep  1 06:30:09 2022, max compression, from Unix, original size modulo 2^32 575
bandit12@bandit:/tmp/bt12$ mv data data2.gz
bandit12@bandit:/tmp/bt12$ gzip -d data2.gz
bandit12@bandit:/tmp/bt12$ ls
data2  data.txt
bandit12@bandit:/tmp/bt12$ file data2
data2: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/bt12$ mv data2 data3.bz
bandit12@bandit:/tmp/bt12$ bzip2 -d data3.bz
bandit12@bandit:/tmp/bt12$ ls
data3  data.txt
bandit12@bandit:/tmp/bt12$ file data3
data3: gzip compressed data, was "data4.bin", last modified: Thu Sep  1 06:30:09 2022, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/bt12$ mv data3 data4.gz
bandit12@bandit:/tmp/bt12$ ls
data4.gz  data.txt
bandit12@bandit:/tmp/bt12$ gzip -d data4.gz
bandit12@bandit:/tmp/bt12$ ls
data4  data.txt
bandit12@bandit:/tmp/bt12$ file data4
data4: POSIX tar archive (GNU)
bandit12@bandit:/tmp/bt12$ mv data4 data5.tar
bandit12@bandit:/tmp/bt12$ tar -xf data5.tar
bandit12@bandit:/tmp/bt12$ ls
data5.bin  data5.tar  data.txt
bandit12@bandit:/tmp/bt12$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/bt12$ mv data5.bin data6.tar
bandit12@bandit:/tmp/bt12$ tar -xf data6.tar
bandit12@bandit:/tmp/bt12$ ls
data5.tar  data6.bin  data6.tar  data.txt
bandit12@bandit:/tmp/bt12$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/bt12$ mv data6.bin data7.bz
bandit12@bandit:/tmp/bt12$ bzip2 -d data7.bz
bandit12@bandit:/tmp/bt12$ ls
data5.tar  data6.tar  data7  data.txt
bandit12@bandit:/tmp/bt12$ file data7
data7: POSIX tar archive (GNU)
bandit12@bandit:/tmp/bt12$ mv data7 data8.tar
bandit12@bandit:/tmp/bt12$ tar -xf data8.tar
bandit12@bandit:/tmp/bt12$ ls
data5.tar  data6.tar  data8.bin  data8.tar  data.txt
bandit12@bandit:/tmp/bt12$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu Sep  1 06:30:09 2022, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/bt12$ mv data8.bin data9.gz
bandit12@bandit:/tmp/bt12$ gzip -d data9.gz
bandit12@bandit:/tmp/bt12$ ls
data5.tar  data6.tar  data8.tar  data9  data.txt
bandit12@bandit:/tmp/bt12$ file data9
data9: ASCII text
bandit12@bandit:/tmp/bt12$ cat data9
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```

## Flag

```wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw```