# 0x08 Cizco's Great Adventure Flag
> 20 (Web)

## Challenge

Cuzco was building her community, talking to others, getting known, making real connections with squirrel buddies, working on balance, and paying attention to her passion for other interests - for her, it was running, but she had one more thing to do: She needed to work on fortitude as she continued her quest to find her Parkour class. Many things in life are not easy and having strength can be helpful. There will be failure along the way. Comparing one’s journey to another person’s can be demoralizing and it is through having a good sense of community and goals that we can make progress. Cuzco knew these things. She practiced reflecting on the progress she’d made since she started her journey…she started with barriers and now there were fewer, she started with walls, and now she had a community, so she grew in her fortitude.

Now that Cuzco had strength from her community and some balance she could test her fortitude. She began work on the digitized file, which was the first thing she gathered on her trip.

Her new friends let her know that she should do some searching. So she opened Command Line (Terminal/Command Prompt/PowerShell) and decided to check the MD5sum of the file Parkour Flyer Information. She’d heard files could be tampered with and she wanted to make sure that hers was safe.

What is the MD5 checksum hash of the downloaded file [Parkour_Flyer_Information.pdf]https://github.com/logicoverflow/ctf/tree/main/sans-new2cyber-ctf/chinchilla/0x08/Parkour_Flyer_Information.pdf) ?

author: [@CarpeDiemT3ch](https://twitter.com/CarpeDiemT3ch)

##  Solution

```
┌──(logicoverflow㉿kali)-[~/Downloads]
└─$ ls
Parkour_Flyer_Information.pdf
                                                                                                                                                        
┌──(logicoverflow㉿kali)-[~/Downloads]
└─$ md5sum Parkour_Flyer_Information.pdf 
9691c69c33f444222facf8fad310aca4  Parkour_Flyer_Information.pdf
```

## Flag

```9691c69c33f444222facf8fad310aca4```
