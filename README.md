<img width="1024" height="271" alt="image" src="https://github.com/user-attachments/assets/d5c66431-4dd4-46f3-aca6-dcea56283ff5" /># OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

<img width="1024" height="729" alt="image" src="https://github.com/user-attachments/assets/168e5a05-b8a5-43dc-b49e-12ea1f769d56" />


cat < file2
## OUTPUT

<img width="1486" height="1059" alt="Neon Terminal Names List (1)" src="https://github.com/user-attachments/assets/d9d2d295-0e7c-4a31-9494-046fba3f3180" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="2170" height="725" alt="Kanishka Terminal Comparison" src="https://github.com/user-attachments/assets/e2085a9a-95fe-4a7f-88ea-da8f4077738f" />

 
comm file1 file2
 ## OUTPUT

<img width="1024" height="791" alt="image" src="https://github.com/user-attachments/assets/374a8ed3-9135-407f-8bad-c9922337c1b2" />

 
diff file1 file2
## OUTPUT

<img width="1024" height="791" alt="image" src="https://github.com/user-attachments/assets/0bc06737-cc4c-4277-b4ed-610c9c266ac3" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
<img width="1024" height="253" alt="image" src="https://github.com/user-attachments/assets/5b4bd2cb-463e-4723-ad48-05a2b048865f" />


cut -c1-3 file11
## OUTPUT

<img width="1024" height="374" alt="image" src="https://github.com/user-attachments/assets/758be31f-5c8f-4d3f-88b3-fe537e1ef707" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="1024" height="374" alt="image" src="https://github.com/user-attachments/assets/2f9b54a5-3686-459c-911d-8d971fb31a50" />


cut -d "|" -f 2 file22
## OUTPUT

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="1024" height="288" alt="image" src="https://github.com/user-attachments/assets/0a67a64d-3690-4b2d-92ae-7043577c68fa" />


grep hello newfile 
## OUTPUT

<img width="1024" height="244" alt="image" src="https://github.com/user-attachments/assets/5d378037-3b55-4ab5-8375-d594fa812fb1" />


grep -v hello newfile 
## OUTPUT

<img width="1024" height="259" alt="image" src="https://github.com/user-attachments/assets/893fa151-1836-4dd2-810a-4263e9e14e26" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="1024" height="181" alt="image" src="https://github.com/user-attachments/assets/e3321231-f820-4179-a854-e99dd369f289" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1024" height="425" alt="image" src="https://github.com/user-attachments/assets/4053c0f4-c891-49da-b789-d84b626c9462" />

grep -R ubuntu /etc
## OUTPUT

<img width="1024" height="252" alt="image" src="https://github.com/user-attachments/assets/7d1fdcf4-1a61-4f51-b706-d1c563a45381" />


grep -w -n world newfile   
## OUTPUT

<img width="1024" height="282" alt="image" src="https://github.com/user-attachments/assets/bd982eeb-6c05-4f6e-9d96-0abf9807b168" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="1024" height="282" alt="image" src="https://github.com/user-attachments/assets/4c85edfe-381e-4c97-b5f8-063a68eb34ea" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="1024" height="290" alt="image" src="https://github.com/user-attachments/assets/13ad59f1-1d4b-473d-8087-2fa12e1e5279" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1024" height="235" alt="image" src="https://github.com/user-attachments/assets/fbd9da59-4067-4f0f-85f3-9bf59be4f639" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="1024" height="278" alt="image" src="https://github.com/user-attachments/assets/2807441f-40cc-41c4-aaa9-221f266529f1" />


egrep '(world$)' newfile 
## OUTPUT

<img width="1024" height="353" alt="image" src="https://github.com/user-attachments/assets/d59769c7-0d74-47c0-b2ac-a0b703ed3142" />


egrep '(World$)' newfile 
## OUTPUT

<img width="1024" height="353" alt="image" src="https://github.com/user-attachments/assets/6c749d3d-d568-4c23-9a8c-8860e65df47e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="1024" height="292" alt="image" src="https://github.com/user-attachments/assets/0ae0c35c-7220-4064-b47c-23b6189620a2" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="1024" height="209" alt="image" src="https://github.com/user-attachments/assets/4dc9047a-27c6-4f61-80f9-154930f26a6b" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="388" height="79" alt="image" src="https://github.com/user-attachments/assets/3dd6004f-98ec-416e-acb6-8c7e781769d0" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="1024" height="329" alt="image" src="https://github.com/user-attachments/assets/ff742b65-7ba9-4921-ad2f-49b81159bdc6" />


egrep l{2} newfile
## OUTPUT

<img width="1024" height="415" alt="image" src="https://github.com/user-attachments/assets/453f62c3-36db-41ea-8c56-35d7850bc57d" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1024" height="627" alt="image" src="https://github.com/user-attachments/assets/894d3022-9507-44c4-894b-55c9cea7d161" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```
<img width="1024" height="627" alt="image" src="https://github.com/user-attachments/assets/dad3172c-99d6-4ec9-9623-0cb4071250c8" />


sed -n -e '3p' file23
## OUTPUT

<img width="359" height="247" alt="image" src="https://github.com/user-attachments/assets/6f52f214-af23-4f28-b758-3d06b2feb278" />


sed -n -e '$p' file23
## OUTPUT

<img width="1024" height="704" alt="image" src="https://github.com/user-attachments/assets/5fb133b8-9acb-4608-a05a-b88967ab7975" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1024" height="617" alt="image" src="https://github.com/user-attachments/assets/044c4c92-efeb-462d-8acc-466d7e944cec" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1295" height="832" alt="image" src="https://github.com/user-attachments/assets/02542fb0-a3d2-4fe8-b629-e58c66358144" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1501" height="704" alt="image" src="https://github.com/user-attachments/assets/8843ab09-81f5-44a7-ba78-d85507d77cbb" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1715" height="624" alt="image" src="https://github.com/user-attachments/assets/2913debd-bd94-4295-9917-9b631214eeac" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1715" height="624" alt="image" src="https://github.com/user-attachments/assets/e0d07a02-48a0-41de-9434-7031297ffbd0" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1024" height="1038" alt="image" src="https://github.com/user-attachments/assets/ae869392-6e23-4706-b6df-77005505e86b" />

seq 10 
## OUTPUT

<img width="1395" height="752" alt="image" src="https://github.com/user-attachments/assets/1c0e2f99-4c35-4a91-9382-954d0dcd38cc" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1619" height="656" alt="image" src="https://github.com/user-attachments/assets/afcd43dd-50df-4655-94d3-6df2f8410994" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1505" height="688" alt="image" src="https://github.com/user-attachments/assets/66448b42-ed12-4c65-a221-b35054096945" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="1475" height="720" alt="image" src="https://github.com/user-attachments/assets/68e56fa0-2cf9-4761-abf1-14ec4dec2cfa" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="1680" height="640" alt="image" src="https://github.com/user-attachments/assets/523f37ba-dd57-4b73-86ea-2f2953118447" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="1796" height="576" alt="image" src="https://github.com/user-attachments/assets/2de8f9ad-a075-4f0f-99b1-48b9303d42bd" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1672" height="624" alt="image" src="https://github.com/user-attachments/assets/c48e80b1-eda3-4e93-a97e-171bb32cb337" />


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="1390" height="752" alt="image" src="https://github.com/user-attachments/assets/43ae2943-2a75-4adb-be21-af16d49ce362" />

sort file21
## OUTPUT

<img width="1418" height="736" alt="image" src="https://github.com/user-attachments/assets/41ede25b-8f3f-4866-a39c-e8b5d73ef919" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

<img width="1477" height="720" alt="image" src="https://github.com/user-attachments/assets/e7fd1fe1-8594-430a-8bd4-4942f50d1c81" />


uniq file22
## OUTPUT

<img width="1390" height="752" alt="image" src="https://github.com/user-attachments/assets/b45bd424-6dbd-49fa-a81f-ba96ec6baa99" />


#Using tr command

<img width="1366" height="784" alt="image" src="https://github.com/user-attachments/assets/4b608d0a-41d3-4f38-99f6-be97353e333e" />


cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="1755" height="608" alt="image" src="https://github.com/user-attachments/assets/5923539b-709b-4b56-bdcf-be1b95993e5d" />


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="1936" height="528" alt="image" src="https://github.com/user-attachments/assets/46c1fc09-bb4c-47be-9c6b-dce7079abb9e" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1066" height="992" alt="image" src="https://github.com/user-attachments/assets/e1a6db60-28ba-4a53-8bcd-9121638268ad" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="1480" height="720" alt="image" src="https://github.com/user-attachments/assets/08d1bbd5-9a0c-49af-9457-e90fddabacc7" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1008" height="1062" alt="image" src="https://github.com/user-attachments/assets/154b45ef-68a8-4592-b6cd-641872f2ceb2" />

tar -xvf backup.tar
## OUTPUT

<img width="1262" height="177" alt="image" src="https://github.com/user-attachments/assets/2e35de22-ea88-4f5a-80d4-1d483d45feeb" />


gzip backup.tar

ls .gz
## OUTPUT



 
gunzip backup.tar.gz
## OUTPUT

<img width="1683" height="624" alt="image" src="https://github.com/user-attachments/assets/b0cbf151-5624-47fc-b080-50b6951ea741" />

 
# Shell Script

<img width="1378" height="768" alt="image" src="https://github.com/user-attachments/assets/d7934f8b-3023-454d-aadf-a882708517c0" />


```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="1488" height="719" alt="image" src="https://github.com/user-attachments/assets/2c39ba66-8509-4715-baa6-4a3387bed4d6" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="1284" height="816" alt="image" src="https://github.com/user-attachments/assets/71c899ad-c8d2-4ab5-b2a1-182b874bbae9" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

<img width="2026" height="512" alt="image" src="https://github.com/user-attachments/assets/476680b7-9d6e-4c2c-9395-89906dcea28b" />

 
ls file1
## OUTPUT

<img width="1925" height="544" alt="image" src="https://github.com/user-attachments/assets/fda8ddf5-ec83-47e8-9fbc-4a489d2f4a2e" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="2076" height="496" alt="image" src="https://github.com/user-attachments/assets/38634694-0360-4229-b2ff-7652e311a70c" />
 
abcd
 
echo $?
 ## OUTPUT

<img width="2076" height="496" alt="image" src="https://github.com/user-attachments/assets/b7b72e30-6ab8-479b-93d3-a1d04d0d1af1" />

 
# mis-using string comparisons

<img width="1344" height="796" alt="image" src="https://github.com/user-attachments/assets/f5227929-43b5-43e9-9c62-ff10917279f6" />


cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT

<img width="2051" height="512" alt="image" src="https://github.com/user-attachments/assets/0a6e1ecf-9416-4167-badd-d02cdbe05497" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="2051" height="512" alt="image" src="https://github.com/user-attachments/assets/dcaef56e-1ca1-48dd-8783-8ca98408e500" />


# check file ownership

<img width="1577" height="656" alt="image" src="https://github.com/user-attachments/assets/1bf601c5-1e07-4562-bdf8-f2c0112e6df9" />


cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location

<img width="1577" height="656" alt="image" src="https://github.com/user-attachments/assets/c4541501-0ebd-4bed-a0b5-435bb9d00330" />


cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

<img width="1043" height="1024" alt="image" src="https://github.com/user-attachments/assets/f13c5395-7908-4044-b416-acb9d6f68827" />


./ifnested.sh 
## OUTPUT

<img width="1079" height="992" alt="image" src="https://github.com/user-attachments/assets/38e799b9-32d7-48d5-8149-3b62fcd831bd" />


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh

<img width="1953" height="544" alt="image" src="https://github.com/user-attachments/assets/43c0df7b-d6f2-44fc-adc9-864a16ef4faa" />

 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

<img width="1904" height="560" alt="image" src="https://github.com/user-attachments/assets/e274c485-a9dd-4927-994d-128823a53417" />


# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT

<img width="2115" height="496" alt="image" src="https://github.com/user-attachments/assets/140d959c-9b19-4b4a-8471-32f2d1caf9e6" />


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

<img width="2124" height="480" alt="image" src="https://github.com/user-attachments/assets/b1bac8f5-bfad-4be5-8ecd-149b8e3f69e0" />



# using the case command

<img width="2382" height="448" alt="image" src="https://github.com/user-attachments/assets/a2db3606-4621-4ba5-99cb-475c2e47a933" />


cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```

<img width="1552" height="688" alt="image" src="https://github.com/user-attachments/assets/9d483d1d-4adb-47af-975f-ea201ca1a7fb" />


$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 <img width="1572" height="656" alt="image" src="https://github.com/user-attachments/assets/aa700b80-475b-4edb-9a74-7fac94ca4da4" />

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh

 <img width="1572" height="656" alt="image" src="https://github.com/user-attachments/assets/4c7db361-40b8-4ad7-9386-5d6d2c256d7f" />

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```

<img width="1663" height="640" alt="image" src="https://github.com/user-attachments/assets/072006de-aa9e-4fa9-808d-09d32c93319d" />


$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```

<img width="1572" height="656" alt="image" src="https://github.com/user-attachments/assets/4da93b98-1254-46ee-a2be-9f5593213417" />


$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```

<img width="1424" height="748" alt="image" src="https://github.com/user-attachments/assets/a952a3e3-0a3e-4642-8355-6bcbcef1c4c3" />


$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

<img width="1487" height="720" alt="image" src="https://github.com/user-attachments/assets/c514b289-c99d-4524-8437-2543834b44b3" />


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```

<img width="1420" height="736" alt="image" src="https://github.com/user-attachments/assets/3ed5ba6d-cbc6-4651-8305-a24dfa7c8844" />


$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

<img width="1954" height="528" alt="image" src="https://github.com/user-attachments/assets/407d4fb5-be52-4aab-929c-a60fe9e1ee46" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

<img width="1613" height="656" alt="image" src="https://github.com/user-attachments/assets/2dc8f594-b213-4e27-8ec5-7364ecd65d45" />


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

<img width="1613" height="656" alt="image" src="https://github.com/user-attachments/assets/998fc96c-6e23-446a-b67d-c23b42fd6cc7" />

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT

<img width="1613" height="656" alt="image" src="https://github.com/user-attachments/assets/052f2721-0b5f-49f1-8a39-db308f768ce0" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="1660" height="640" alt="image" src="https://github.com/user-attachments/assets/4773e80f-5a5d-4bc6-87e3-603011c94238" />


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT

<img width="1617" height="656" alt="image" src="https://github.com/user-attachments/assets/832a7385-25d0-4b80-85f1-46719d3f18ad" />


 ./funcex.sh 

<img width="2308" height="464" alt="image" src="https://github.com/user-attachments/assets/72cf53e9-394b-4f5d-9323-edd95e74302b" />

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
<img width="1411" height="752" alt="image" src="https://github.com/user-attachments/assets/c8e612c6-0c1d-4c85-9b73-960fac5a96fc" />


$ chmod 777 argshift.sh

## OUTPUT

<img width="1444" height="736" alt="image" src="https://github.com/user-attachments/assets/ccdb7093-d726-480b-8586-9ce65e1eaefc" />


$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT

<img width="1045" height="1008" alt="image" src="https://github.com/user-attachments/assets/03e3bcc0-a41e-4341-9160-62cf9fe4f0f5" />


$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```

<img width="1040" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5973e49-3abc-464b-aeed-9bfba2daa6c2" />


awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 

<img width="1173" height="912" alt="image" src="https://github.com/user-attachments/assets/774956eb-a6a1-418d-a26c-b109e7a9b1d3" />



# RESULT:
The Commands are executed successfully.
