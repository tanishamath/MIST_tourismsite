# Bandit Over the Wire
![Rules](https://media.discordapp.net/attachments/858349899401658398/1296049271187046443/image.png?ex=6710df71&is=670f8df1&hm=09168a3e9fb587b22077712282931f09f3ee8f075a0f4a21bc833f4b53a79abc&=&format=webp&quality=lossless&width=1407&height=593)
## Level 0
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295136534969974915/image.png?ex=670d8d64&is=670c3be4&hm=8387b4863059ab8ff91938d2a8d410eb7f8b1a4ea3283145f70e75aad66d6c32&=&format=webp&quality=lossless&width=1440&height=308)
### Solution : 
```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
We log into the game using SSH.   
We keep on finding the password by solving challenges.  
In this level, the password is already given in the question.
### Password : 
```
bandit0
```

## Level 0 -> Level 1
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295137664499974194/image.png?ex=670d8e71&is=670c3cf1&hm=af7b0759fcb958082289e13df9d7b95b8d2ed867af974005a7ebcebdc07c7a5e&=&format=webp&quality=lossless&width=1440&height=392)
### Solution : 
```
ls
```
We look for the files in the directory and find a file readme.
```
cat readme
```
We read the content of readme using cat. This gives us the password.
### Password : 
```
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

## Level 1 -> Level 2
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295138799252279337/image.png?ex=670d8f80&is=670c3e00&hm=83fa710859ecd019ac59e35d9ae4e5d942271661691e8c5ee5c6bc616093f033&=&format=webp&quality=lossless&width=1440&height=360)
### Solution : 
```
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
cat ./-
```
We read the content of the file "-" by explicitly writing its path in the current directory using ./ .   
This gives us the password.
### Password : 
```
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

## Level 2 -> Level 3
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295140322732412968/image.png?ex=670d90eb&is=670c3f6b&hm=3fd75517e1704e7154a535757d469cea73b3f4b3a3dfc1b7edb035c2f7b41f0b&=&format=webp&quality=lossless&width=1440&height=352)
### Solution : 
```
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
cat spaces\ in\ this\ filename
```
We read the content of the file "spaces in this filename" by using / followed by a whitespace to signify the presence of a whitespace in the file name.
This gives us the password.
### Password : 
```
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

## Level 3 -> Level 4
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295141143159504948/image.png?ex=670d91af&is=670c402f&hm=43aa18baf274c4cb6859ccb06f46590df6039a0f65f842e28e65deb65ebb98d1&=&format=webp&quality=lossless&width=1440&height=208)
### Solution : 
```
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
ls -a inhere/
```
We use ls -a to view all the files (including hidden files) in the "inhere" directory.
```
cat ...Hiding-From-You
```
This gives us the password as we read the hidden file.
### Password : 
```
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

## Level 4 -> Level 5
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295142105622122567/image.png?ex=670d9294&is=670c4114&hm=c6cf595560ffb69206ef3cb02881de9b64e4c571e1587d335e55ebc9d856070a&=&format=webp&quality=lossless&width=1440&height=225)
### Solution : 
```
ssh bandit4@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
cd inhere/
```
We change our directory to inhere.
```
ls
```
We check the contents of inhere.
```
file ./-file00
```
We keep repeating this command for all files from -file00 to -file08 until we encounter a filetype that is not data.  
We find this when we reach -file07 where we see that filetype is ASCII text.
```
cat ./-file07
```
We get the password on reading the content of -file07.
### Password : 
```
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

## Level 5 -> Level 6
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295143846996480001/image.png?ex=670d9433&is=670c42b3&hm=2ce754a4553e351fbaf673fa69fd1b1a6c6598772300baccd286c8efa1751362&=&format=webp&quality=lossless&width=1440&height=316)
### Solution : 
```
ssh bandit5@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
cd inhere/
```
We change our directory to inhere.
```
ls
```
We check the contents of inhere.
```
find . -type f -size 1033c
```
We use "." to make the find command go through all files in the directory.  
We use -type f to signify that we want to find a file.  
We use -size 1033c to search for the file which is 1033 bytes in size.  
The find command with these specifications finds the file we need.
```
cat ./maybehere07/.file2
```
This gives us the password.
### Password : 
```
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

## Level 6 -> Level 7
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295145753039343649/image.png?ex=670d95fa&is=670c447a&hm=7b3b71bc373d67c120e1ab710de8ef49ed28651a71a0b2c1d77f18872c3c0e6c&=&format=webp&quality=lossless&width=1440&height=312)
### Solution : 
```
ssh bandit6@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```
We use "/" to make the find command go through all files in the root directory.  
We use -user bandit7 to search for files where the user bandit7 has access. 
We use -group bandit6 to search for files where the group bandit6 has access. 
We use -size 33c to search for the file which is 33 bytes in size. 
We redirect all the the errors we encounter (denied permission) to /dev/null which essentially supresses the errors we get.
The find command with these specifications finds the file we need.
```
cat /var/lib/dpkg/info/bandit7.password
```
This gives us the password.
### Password : 
```
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

## Level 7 -> Level 8
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295313417468645407/image.png?ex=670e3220&is=670ce0a0&hm=1b5c9c4c88f734962e0e3ab727ac49a9c68fc776716297af14cc4a0b10843351&=&format=webp&quality=lossless&width=1440&height=230)
### Solution : 
```
ssh bandit7@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
grep millionth data.txt
```
We use grep to find the occurences of the string "millionth" in the file data.txt.  
This gives us the password.
### Password : 
```
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```

## Level 8 -> Level 9
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295314466937770025/image.png?ex=670e331a&is=670ce19a&hm=82b8d5e00d3a77fa93024778ac97b6abdfdb6ef71389433a11a40da9ce419167&=&format=webp&quality=lossless&width=1440&height=320)
### Solution : 
```
ssh bandit8@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
sort data.txt | uniq -u
```
We use sort to group together all the identical strings in the file since the command uniq -u can only detect presence of consecutive identical strings.  
We pipe this standard output into the standard input of uniq -u (using |) to filter out all the strings that have atleast one repetition, leaving us with a single unique string.  
This string is the password.
### Password : 
```
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```

## Level 9 -> Level 10
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295316866562261072/image.png?ex=670e3556&is=670ce3d6&hm=398c9b54e67b013aa29bbc7aa5dfeccee6b5699be6d276ac37209c62b9cef74f&=&format=webp&quality=lossless&width=1440&height=212)
### Solution : 
```
ssh bandit9@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
strings data.txt | grep '=='
```
We use strings to gather all the human readable strings present in the file.  
We pipe the standard output of strings command to the standard input of grep command.  
Since it is mentioned that there are several '=' characters, there must be atleast 2 consecutive occurences and that is what we pass as argument of grep.  
This gives us the password.
### Password : 
```
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```

## Level 10 -> Level 11
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295318735997108306/image.png?ex=670e3714&is=670ce594&hm=6daea837380efded9bec6b4e387700807b13ad1ef8cd86c5ac4f686a97cc764c&=&format=webp&quality=lossless&width=1440&height=317)
### Solution : 
```
ssh bandit10@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
base64 -d data.txt
```
This command decodes the base64-encoded data back to its original form which gives us the password.
### Password : 
```
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```

## Level 11 -> Level 12
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295320019529371739/Screenshot_2024-10-14_150856.png?ex=670e3846&is=670ce6c6&hm=9b5d2540e01c2f63d38f9734232c2d334664a683c90536b4be3f8a42608ca7cd&=&format=webp&quality=lossless&width=1440&height=311)
### Solution : 
```
ssh bandit11@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
cat data.txt
```
We read the contents of the file which gives us the ROT13 substitution cypher. We must decode this to get the password.  
The content of the file : Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4  
We use the following chart for decoding :  
![ROT13 Chart](https://media.discordapp.net/attachments/858349899401658398/1295322044438679582/ROT13.png?ex=670e3a29&is=670ce8a9&hm=1b869933f4afedc778138863a5cf26670e79adba90a8dabdd6cf47822bb8d474&=&format=webp&quality=lossless&width=750&height=182)   
Decoding gives us the following message : The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
### Password : 
```
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```

## Level 12 -> Level 13
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295323262502567998/image.png?ex=670e3b4b&is=670ce9cb&hm=dbf6a31743c2c3591e96dd52b344dbdbe97d16003812c8eaba2827b1e5aa33c3&=&format=webp&quality=lossless&width=1440&height=362)
### Solution : 
```
ssh bandit12@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
mkdir /tmp/brooooo
```
We create a new directory in tmp for our own convenience.
```
cp /home/bandit12/data.txt /tmp/brooooo
```
We copy our data file to the directory we just created.
```
mv data.txt comp.hex
```
We convert our file from txt to hexdump using mv to rename.
```
xxd -r comp.hex comp.bin
```
We reverse the hexdump back to the binary using xxr -r where -r signifies reversing.
```
file comp.bin
```
We get to know that the filetype is gzip compressed data.
``` 
mv comp.bin ans.gz
```
We rename our file to add the .gz extension in order to unzip.
```
gunzip ans.gz
```
We decompress the file.
```
file ans
```
We get to know that the filetype is bzip2 compressed data.
```
bunzip2 ans
```
We decompress the file.
```
file ans.out
```
We get to know that the filetype is gzip compressed data.
```
mv ans.out ans.gz
```
We rename our file to add the .gz extension in order to unzip.
```
gunzip ans.gz
```
We decompress the file.
```
file ans
```
We get to know that the filetype is POSIX tar archive.
```
mv ans ans.tar
```
We rename the file to add the .tar extension
```
tar xvf ans.tar
```
We extract the contents of the TAR archive to get the bin file.
```
file data5.bin
```
We get to know that the filetype is POSIX tar archive.
```
mv data5.bin ans.tar
```
We rename the file to add the .tar extension.
```
tar xvf ans.tar
```
We extract the contents of the TAR archive to get the bin file.
```
file data6.bin
```
We get to know that the filetype is bzip2 compressed data.
```
bunzip2 data6.bin
```
We decompress the file.
```
file data6.bin.out
```
We get to know that the filetype is POSIX tar archive.
```
mv data6.bin.out ans.tar
```
We rename the file to add the .tar extension.
```
tar xvf ans.tar
```
We extract the contents of the TAR archive to get the bin file.
```
file data8.bin
```
We get to know that the filetype is gzip compressed data.
```
mv data8.bin ans.gz
```
We rename our file to add the .gz extension in order to unzip.
```
gunzip ans.gz
```
We decompress the file.
```
file ans
```
We get to know that the filetype is human readable ASCII text.
```
cat ans
```
This gives us the password.
### Password : 
```
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```

## Level 13 -> Level 14
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295386758653018172/image.png?ex=670e766e&is=670d24ee&hm=54f3fcc07350313facba3f225c37174a8479728e2dc065970553880749e7316e&=&format=webp&quality=lossless&width=1440&height=352)
### Solution : 
```
ssh bandit13@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
ls
```
We check the contents to look for the SSH private key file.
```
ssh -i sshkey.private bandit14@localhost -p 2220
```
A secure shell client is invoked by ssh.  
We append -i to signify that we must use the identity of the private key for authentication.  
Here, bandit14 is the username for the next challenge.  
We use localhost to refer to the local machine, meaning we connect to the same server we are currently on.  
We use -p 2220 to connect to port 2220.
### Password :
Initially we do not get the password but we do get the password from the next level.
```
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```

## Level 14 -> Level 15
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295389368860676117/image.png?ex=670e78dc&is=670d275c&hm=4910e15a7a33915e93b40a33a7f417512034252a685ead5cd602be31ffa907f9&=&format=webp&quality=lossless&width=1440&height=468)
### Solution : 
```
ssh bandit14@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
cat /etc/bandit_pass/bandit14
```
This gives us the password for the current level.
```
echo "MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS" | nc localhost 30000
```
We pipe the standard output of the echo command into the standard input of the netcat command which connects us to the port 30000 which receives the password for the next level in response.
### Password : 
```
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```

## Level 15 -> Level 16
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295392245532594268/image.png?ex=670e7b8a&is=670d2a0a&hm=14f79386fca32549bc99baa15a5a002919b7462e516cb5a1cc994813d4686ffe&=&format=webp&quality=lossless&width=1440&height=396)
### Solution : 
```
ssh bandit16@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
openssl s_client -connect localhost:30001
```
We write openssl for using various cryptographic functions of OpenSSL.  
We use s_client to signify that we wish to operate as a client for the SSL/TLS connection.  
Localhost is the name of our local machine.  
30001 is the port number we want to port to.  
When we reach the part where we see the prompt "read R BLOCK", we enter the password of the current level.  
This gives us the password.
### Password : 
```
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```

## Level 16 -> Level 17
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1295402113706229864/image.png?ex=670e84bb&is=670d333b&hm=faa55fec2652ec8cdf96df0955210dae8e7ed277f78d5c7efbadc24f3db8977c&=&format=webp&quality=lossless&width=1440&height=406)
### Solution : 
```
ssh bandit16@bandit.labs.overthewire.org -p 2220
```
We log into the level using SSH and the password obtained from the last level.
```
nmap localhost -p 31000-32000
```
This scans the localhost for open network ports in the range of 31000 to 32000.
```
ncat --ssl localhost 31790
```
We keep on trying the command ncat --ssl localhost (port number) for all the open ports until we get a response from the port.  
After entering the command, we enter our password.  
On the port 31790, once we enter the password we get a private RSA key which will help us progress to the next level.
```
exit
```
We exit the bandit localhost and go back to our own machine.
```
nano bandit17key
```
We create a new file and we input the RSA key we just obtained.
```
chmod u=rwx bandit17key
```
We change the permissions of the file to grant read, write and execute permission to us (the user).
### Password : 
Instead of getting the password directly, we get the private RSA key to progress to the next level.
```
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
```

## Level 17 -> Level 18
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1296044674167078912/image.png?ex=6710db29&is=670f89a9&hm=65d78671275af7ae007261f2cc5edbbe6a5a352a283e9d60a0c7b654c409157d&=&format=webp&quality=lossless&width=1440&height=285)
### Solution : 
```
ssh -i bandit17key bandit17@bandit.labs.overthewire.org -p 2220
```
We use the private RSA key from the previous level to login to this level.  
here, bandit17key is the file containing the key.
```
diff passwords.old passwords.new
```
This compares the contents of the two files and shows the differences between them.  
The string followed by < is the unique string in passwords.old.  
The string followed by > is the unique string in passwords.new which is our password in this case.
### Password : 
```
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
```

## Level 18 -> Level 19
### Problem : 
![Question](https://media.discordapp.net/attachments/858349899401658398/1296046773068107806/image.png?ex=6710dd1e&is=670f8b9e&hm=acdb82181b124d417709893a7cacb89e9658cff3aa2345a712e66617dfae087a&=&format=webp&quality=lossless&width=1440&height=225)
### Solution : 
```
ssh bandit18@bandit.labs.overthewire.org -p 2220 'cat readme'
```
Since we get logged out everytime we try to login with the ssh, we directly pass the command we want to run by enclosing it within ' ' so that we can directly get the flag before getting logged out.  
The readme file contains our password.
### Password : 
```
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
```




