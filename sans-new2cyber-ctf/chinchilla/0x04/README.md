# 0x04 Cuzco's Great Adventure Flag
> 20 (Stego, OSINT)

## Challenge

Flag 4 Use the image file to find the question:

[Download Here](https://github.com/logicoverflow/sans-new2cyber-ctf/blob/main/chinchilla/0x04/believe_with_layers.png)

## Solution

**Steganography portion:**

```
┌──(logicoverflow㉿ALNLPTRV)-[~]
└─$ strings believe_with_layers.png | grep FLAG
"FLAG 4 Question: Use OSINT, Who invented Parkour?"
"FLAG 5 Question: Use OSINT, What do you call someone who does Parkour?"
```

**OSINT portion:**

![David Belle](https://github.com/logicoverflow/sans-new2cyber-ctf/blob/main/chinchilla/0x04/firefox_k4vmQjnON8.png)

## Flag

```David Belle```
