# overthewire
Write up for wargame Bandit
https://overthewire.org/wargames/bandit/

## Level 0 
ssh bandit0@bandit.labs.overthewire.org -p 2220 password:bandit0

## Level 0->1
cat readme
Password:boJ9jbbUNNfktd78OOpsqOltutMc3MY1

## Level 1->2
ssh bandit1@bandit.labs.overthewire.org -p 2220

cat ./-
Password:CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

## Level 2->3
ssh bandit2@bandit.labs.overthewire.org -p 2220

cat spaces\ in\ this\ filename

Password:UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

## Level 3->4
ssh bandit3@bandit.labs.overthewire.org -p 2220

$ cd inhere
$ find
$ cat .hidden

Password:pIwrPrtPN36QITSp3EQaw936yaFoFgAB

## Level 4->5
ssh bandit4@bandit.labs.overthewire.org -p 2220

$ cd inhere
$ file "all files"
Then cat the file that has the filetype 'ASCII text'
$ cat ./-file07

Password:koReBOKuIDDepwhWk7jZC0RTdopnAYKh

## Level 5->6
ssh bandit5@bandit.labs.overthewire.org -p 2220

Find of type 'file' with precis size of 1033byte, and then cat the file. https://ostechnix.com/find-files-bigger-smaller-x-size-linux/
$ find . -type f -size 1033c -exec cat {} +

Password:DXjZPULLxYr17uwoI01bNLQbtFemEgo7

## Level 6->7
ssh bandit6@bandit.labs.overthewire.org -p 2220

$ find / -type f -size 33c -group bandit6 -user bandit7

$ cat /var/lib/dpkg/info/bandit7.password

Password:HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

## Level 7->8
ssh bandit7@bandit.labs.overthewire.org -p 2220

$ cat data.txt | grep millionth

Password:cvX2JJa4CFALtqS87jk27qwqGhBM9plV

## Level 8->9
ssh bandit8@bandit.labs.overthewire.org -p 2220

First sort the passwords then count the number of occurrences, and last grep the password with only one occurrence.
$ cat data.txt | sort | uniq -c | grep '1 '

Another solution: 
$ cat data.txt | sort | uniq -u

Password:UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

# Level 9->10
ssh bandit9@bandit.labs.overthewire.org -p 2220

Print all readable strings and grep the ones with '=='
$ cat data.txt | strings -a | grep '=='

Password:truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

# Level 10->11
ssh bandit10@bandit.labs.overthewire.org -p 2220

$ cat data.txt | base64 -d

Password:IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

# Level 11->12
ssh bandit11@bandit.labs.overthewire.org -p 2220

$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

Password:5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

# Level 12->13
ssh bandit12@bandit.labs.overthewire.org -p 2220

Creating temp. folder
$ mkdir /tmp/iamwinning2020

Copy data.txt to new folder
$ cp data.txt /tmp/iamwinning2020/data.txt

First hexdump to compressed file
$ xxd -r data.txt data1

Then alternate between the following to decompress
$ gunzip {filename}
$ bunzip2 {filename}
$ tar -xf {filename}

Use $ file {filename} to check the file type. Sometimes file renaming is needed, then use $ mv {old filename} {new filename}.

Keep decompressing until the file type is off 'ASCII text'

Password:8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

# Level 13->14
ssh bandit13@bandit.labs.overthewire.org -p 2220

Login to bandit14 using the private key
$ ssh -i sshkey.private bandit14@localhost

Password:4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

# Level 14->15
ssh bandit13@bandit.labs.overthewire.org -p 2220 or login through level 13

$ cat /etc/bandit_pass/bandit14 | telnet localhost 30000 Or $ cat /etc/bandit_pass/bandit14 | nc localhost 30000

Password:BfMYroe26WYalil77FoDi9qh59eK5xNr

# Level 15->16
ssh bandit15@bandit.labs.overthewire.org -p 2220

$ cat /etc/bandit_pass/bandit15 | openssl s_client -ign_eof -connect localhost -port 30001

Password:cluFn7wTiGryunymYOu4RcffSxQluehd

# Level 16->17
ssh bandit16@bandit.labs.overthewire.org -p 2220

$ cat /etc/bandit_pass/bandit16 |  openssl s_client -connect localhost -port 31790 -ign_eof -quiet 1> /tmp/jalocin2020/private17.key

Remove the top line "Correct!"
$ nano /tmp/jalocin2020/private17.key

Change privileges
$ chmod 400 /tmp/jalocin2020/private17.key

SSH into bandit17
ssh -i /tmp/jalocin2020/private17.key bandit17@bandit.labs.overthewire.org -p 2220

Private key:
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

# Level 17->18
ssh bandit17@bandit.labs.overthewire.org -p 2220

$ diff passwords.new passwords.old

Password:kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

# Level 18->19
ssh bandit18@bandit.labs.overthewire.org -p 2220

$ ssh -t bandit18@bandit.labs.overthewire.org -p 2220 bash --norc --noprofile

$ cat readme

Or

$ ssh bandit18@bandit.labs.overthewire.org -p 2220 'cat readme'

Password:IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

# Level 19->20
ssh bandit19@bandit.labs.overthewire.org -p 2220

$ ./bandit20-do cat /etc/bandit_pass/bandit20

Password:GbKksEFF4yrVs6il55v6gwY5aVje5f0j

# Level 20->21
ssh bandit20@bandit.labs.overthewire.org -p 2220

$ nc -lvp 20000 // and paste bandit20 password

In other window(Might use 'screen' tool)
$ ./suconnect 20000

Password is printed in the first window.

Password:gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

# Level 21->22
ssh bandit21@bandit.labs.overthewire.org -p 2220


Password:Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI

# Level 22->23
ssh bandit22@bandit.labs.overthewire.org -p 2220


Password:jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n

# Level 23->24
ssh bandit23@bandit.labs.overthewire.org -p 2220


Password:UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ

# Level 24->25
ssh bandit24@bandit.labs.overthewire.org -p 2220