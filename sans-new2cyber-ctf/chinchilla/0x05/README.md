# 0x05 Cuzco's Great Adventure Flag
> 20 (Stego, OSINT)

## Challenge

Flag 5 Use the image file to find the question:

[Download Here](https://github.com/logicoverflow/ctf/blob/main/sans-new2cyber-ctf/chinchilla/0x05/believe_with_layers.png)

## Solution

**Steganography portion:**

```
┌──(logicoverflow㉿ALNLPTRV)-[~]
└─$ strings believe_with_layers.png | grep FLAG
"FLAG 4 Question: Use OSINT, Who invented Parkour?"
"FLAG 5 Question: Use OSINT, What do you call someone who does Parkour?"
```

**OSINT portion:**

![traceur](https://github.com/logicoverflow/ctf/blob/main/sans-new2cyber-ctf/chinchilla/0x05/firefox_fsgUbS4rbB.png)

## Flag

```traceur```
