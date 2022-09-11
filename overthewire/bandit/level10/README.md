# Level 10

## Challenge

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

Reference: [Bandit Level 10](https://overthewire.org/wargames/bandit/bandit10.html)

#### Commands you may need to solve this level

```grep```, ```sort```, ```uniq```, ```strings```, ```base64```, ```tr```, ```tar```, ```gzip```, ```bzip2```, ```xxd```

## Solution

```
┌──(logicoverflow㉿RZR-LP)-[~]
└─$ ./bandit.sh 9
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit9@bandit.labs.overthewire.org's password:

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

bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ head data.txt
�f��`����R\S�;*1}Kf��!�`�L`�Ƌ��W�d���rE�;�N�A0�r=w�֦�४`T#n!O�
�dz*�N)�Cr�9_m�Մ0��w0M��H�n��ѿ������!�1
                                               �? ۉ�B�R_�ex_���z!d2�m(K��r�=��3�jI�1�3��J��a�ʴ[��3;�����,�~k���R1�w�7 ��G��1�JY�x0&�bjM�:�:].�z��#�)y�2%�      ��$�U\����?Ƶ������U'�{��I~�aŦ`�#��sl�G �ȭ[L�t�q�.|���C=ҾDG��m�;��i�Y3u0�V�ș��Ή�#�w�m������'��1P�Z�l���ȭV���'�Own���       �1�D!P�yX��K�"=id6�S�1�FJ�"�-�pjΡ��D�O�XW�O�7�i���5��?jF���ƭ�m*g��no�����c.��SD����J������e�r��*�[(V#�;B��.�KY�D2�
S�hC
��f~�>ځ
 pX����z)ȶ=K�[�

             �!p�a��L6'�c������r��뙕��:;������N:��2u��zp<�8��TѼ�E4�=�2=�?aT��;ȹC���
                                                                                         ��w�đ���ӘG��IkSR3(8|  ��M�   �11u"�@*�;�Kw5-T��2     j6.4�/��w7+R��3����
                                            ���
                                               ��cksQ��Gsb�j���b�}|֨����9�����2���J *��@�Jwh(�h�J}�:=�/R>�1�BEo�D!_�xa�¬ҍ�ٸ5T�t�sJ�f��9�-q|?v��       ������z�]%*���(A�f�P)���ɤ}!��
��wꝭ�*                                                                   ��sa�xPAF�f�ͤK`
�      H�bd]?G��v~�k�j�gi�mmS�a;h����l�n
                                             a��1�XG�L��چ�C/�C�˷�����C��� c��m�Ė�+Q-Ϋ�
                                                                                         ����M������========== the�@��%�����T�Ә�1��O��J#g��STY5�
                   }��
�Ԙ���X3y9�����,�6��_خ�4�BJf��'��օ,�N�Lə�
6��̧�XG��x����$C�I�8V��I̸W���"ˌ��/��M��
                                              9.� �|��3���TW"�X����v��M��>܉1�ڔ?m@����~%�T�
                                                                                                <�+�r�1+�g�����4��C�J�Ч���W�s��H�k5��pޠ��3��8#`�+�'Q�������4���M<?Q��(��)l����]R�A�!������@���+v((�6>
                                                                                     �S��
                                                                                           P�4\�Xm�>���ݫ�d��mB��Q9�4<w��p���=�%�{�賆�W.�)�Q1�ΣF��;�.7b�E+�68��6�
                                           ��ۑ�o��޾�>y �۱{/�D�d�U�l�r�b�jp���q�r>���
                                                                                      �~�y^�9������]�H�����ѫ�d�A}�B4��0��jG���6�%:8�J:�����oכ���
                                @����#c��4��>���]b��~c0���H����vt����7ր�l=�U�
                                                                               �s4�*>O�,a��
í�2�_Zc����
2�q�����(IG�]�?oq�=�6�%qdcR;�?�E�,�9�Dh�x����q�?>H`J�M����J����ͥVV8�]��!�Ds��`��*=օl�gO=89�]y
                                                                                                   �&d� |<?����
                                                                                                               �
���7T��A��LCG� b�&v*��[�N�77�A�deG3KZ����)�����P��BJƉ>t���jS��#� �
bandit9@bandit:~$ strings data.txt | grep ===
========== the
bu========== password
4iu========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

## Flag

```G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s```