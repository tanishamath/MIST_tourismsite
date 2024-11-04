# PicoCTF
![s02061111052024](https://a.okmd.dev/md/6729303e2d111.png)
## 1. Vigenere
### Problem : 
![s23330011042024](https://a.okmd.dev/md/67290c56aed33.png)
### Solution : 
We open the website https://www.dcode.fr/en.  
We search for vigenere cypher as provided in the question.  
We enter the cyphertext and the key in the fields provided.  
This decodes the cypher and gives us the flag.
![s23364511042024](https://a.okmd.dev/md/67290d382d093.png)
### Password : 
```
picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_d85729g7}
```

## 2. Easy1
### Problem : 
[s23375611042024](https://a.okmd.dev/md/67290d7e5830f.png)
### Solution : 
We first check out the table provided to us.
```
    A B C D E F G H I J K L M N O P Q R S T U V W X Y Z 
   +----------------------------------------------------
A | A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
B | B C D E F G H I J K L M N O P Q R S T U V W X Y Z A
C | C D E F G H I J K L M N O P Q R S T U V W X Y Z A B
D | D E F G H I J K L M N O P Q R S T U V W X Y Z A B C
E | E F G H I J K L M N O P Q R S T U V W X Y Z A B C D
F | F G H I J K L M N O P Q R S T U V W X Y Z A B C D E
G | G H I J K L M N O P Q R S T U V W X Y Z A B C D E F
H | H I J K L M N O P Q R S T U V W X Y Z A B C D E F G
I | I J K L M N O P Q R S T U V W X Y Z A B C D E F G H
J | J K L M N O P Q R S T U V W X Y Z A B C D E F G H I
K | K L M N O P Q R S T U V W X Y Z A B C D E F G H I J
L | L M N O P Q R S T U V W X Y Z A B C D E F G H I J K
M | M N O P Q R S T U V W X Y Z A B C D E F G H I J K L
N | N O P Q R S T U V W X Y Z A B C D E F G H I J K L M
O | O P Q R S T U V W X Y Z A B C D E F G H I J K L M N
P | P Q R S T U V W X Y Z A B C D E F G H I J K L M N O
Q | Q R S T U V W X Y Z A B C D E F G H I J K L M N O P
R | R S T U V W X Y Z A B C D E F G H I J K L M N O P Q
S | S T U V W X Y Z A B C D E F G H I J K L M N O P Q R
T | T U V W X Y Z A B C D E F G H I J K L M N O P Q R S
U | U V W X Y Z A B C D E F G H I J K L M N O P Q R S T
V | V W X Y Z A B C D E F G H I J K L M N O P Q R S T U
W | W X Y Z A B C D E F G H I J K L M N O P Q R S T U V
X | X Y Z A B C D E F G H I J K L M N O P Q R S T U V W
Y | Y Z A B C D E F G H I J K L M N O P Q R S T U V W X
Z | Z A B C D E F G H I J K L M N O P Q R S T U V W X Y
```
We check the cyphertext and match it with the alphabets on the row side.  
We then traverse the row and look for the key in the row.  
Then traverse the column and look for the alphabet which is on the top of the column.   
This alphabet gives us our decrypted message which is our flag.
### Password : 
```
picoCTF{CRYPTOISFUN}
```

## 3. Ready Gladiator 0
### Problem : 
![s00422211052024](https://a.okmd.dev/md/67291c9962fd0.png)
### Solution : 
Download the source code which gives us the imp.red.  
We cat the file which gives us the source code :
```
;redcode
;name Imp Ex
;assert 1
mov 0, 1
end
```
We must change this source code such that we allow no ties or lies. The new code is now:
```
;redcode
;name Self-Destruct
;assert 1
DAT 0, 0    ; DAT kills the process immediately
end
```
We then write the command which gives us the flag :
```
nc saturn.picoctf.net 62378 < imp.red
```
![s00490811052024](https://a.okmd.dev/md/67291e2eb4ff2.png)
### Password : 
```
picoCTF{h3r0_t0_z3r0_4m1r1gh7_7c030e56}
```

## 4. Verify
### Problem : 
![s01033311052024](https://a.okmd.dev/md/6729219021989.png)
### Solution : 
We want to find the correct file containing the flag by matching its SHA-256 checksum to the given checksum.  
We get the checksum by catting the file, which is 55b983afdd9d10718f1db3983459efc5cc3f5a66841e2651041e25dec3efd46a.  
For each file, we want to calculate the SHA-256 hash and compare it with the given checksum. We can automate this using:
```
for file in files/*; do
    sha256sum "$file" | grep "55b983afdd9d10718f1db3983459efc5cc3f5a66841e2651041e25dec3efd46a" && echo "Found: $file"
done
```
This gives us our required file 2cdcb2de and we decrypt this, which gives us the flag.
![s01041611052024](https://a.okmd.dev/md/672921badf51f.png)
![s01045211052024](https://a.okmd.dev/md/672921dfdbbb2.png)
### Password : 
```
picoCTF{trust_but_verify_2cdcb2de}
```

## 5. Mob psycho
### Problem : 
![s01554311052024](https://a.okmd.dev/md/67292dc9ae52f.png)
### Solution : 
Firstly we download the apk.  
Then on the terminal we unzip the apk.  
Then we look for the file which contains the word flag as it can lead us to the flag.
![s01580211052024](https://a.okmd.dev/md/67292e53ee741.png)
We take the string and go to the site https://scwf.dima.ninja/ .  
This site helps us to brute force our answer by taking into account the frequency of words in the english language.  
Thus we get the flag.
![s02072111052024](https://a.okmd.dev/md/67293082dbea7.png)
### Password : 
```
picoCTF{ax8mC0RU6ve_NX85l4ax8mCl_a3eb5ac2}
```

