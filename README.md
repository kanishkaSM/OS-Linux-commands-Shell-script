# OS-Linux-commands-Shell-scripting
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

<img width="3162" height="340" alt="image" src="https://github.com/user-attachments/assets/f47b83bc-7169-45f9-b0db-6e6c21acbfdf" />


cat < file2
## OUTPUT

<img width="3162" height="408" alt="image" src="https://github.com/user-attachments/assets/e8f02a04-e840-43ed-87aa-408f0ad1e519" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="3186" height="136" alt="image" src="https://github.com/user-attachments/assets/971c676e-0638-45a5-8f62-0df340587a95" />


 
comm file1 file2
 ## OUTPUT

<img width="3162" height="606" alt="image" src="https://github.com/user-attachments/assets/12156627-c52a-4d19-bee7-de2a0ce3b563" />

 
diff file1 file2
## OUTPUT

<img width="3162" height="666" alt="image" src="https://github.com/user-attachments/assets/82571b84-5fe4-44a0-93b0-660904f6ef20" />


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


cut -c1-3 file11
## OUTPUT

<img width="3162" height="212" alt="image" src="https://github.com/user-attachments/assets/609e53a4-9cdf-4c3f-99fd-04b376c96ec5" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="3338" height="278" alt="image" src="https://github.com/user-attachments/assets/47dbd709-93aa-4453-84fa-d280847e81c5" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="3338" height="278" alt="image" src="https://github.com/user-attachments/assets/491476ef-910c-4324-9f2d-7da7880ad9cc" />


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

<img width="3338" height="140" alt="image" src="https://github.com/user-attachments/assets/fb6635ae-1ba2-487b-8f4a-4b167abdf190" />



grep hello newfile 
## OUTPUT

<img width="3338" height="140" alt="image" src="https://github.com/user-attachments/assets/628e6213-56b6-4725-8f3e-3935040239fb" />


grep -v hello newfile 
## OUTPUT

<img width="3338" height="140" alt="image" src="https://github.com/user-attachments/assets/533687da-f28e-42b7-a7b9-67d54fc06514" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="3562" height="208" alt="image" src="https://github.com/user-attachments/assets/491d4d6f-dac8-4387-9471-c71eb05b4f13" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="3654" height="144" alt="image" src="https://github.com/user-attachments/assets/b5a48196-ddc3-482e-999c-704699212e5b" />



grep -R ubuntu /etc
## OUTPUT

<img width="2216" height="142" alt="image" src="https://github.com/user-attachments/assets/b13c843a-f670-4dad-b190-c2792d4fcc33" />



grep -w -n world newfile   
## OUTPUT

<img width="2216" height="142" alt="image" src="https://github.com/user-attachments/assets/71a91a5c-a7a4-46ad-b896-67e5abc782f6" />



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

<img width="2344" height="142" alt="image" src="https://github.com/user-attachments/assets/521d333b-6a49-4992-a781-1524c8671bf1" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="2344" height="142" alt="image" src="https://github.com/user-attachments/assets/0842c519-33ca-43e6-a2cd-c183d41cd542" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="2382" height="142" alt="image" src="https://github.com/user-attachments/assets/c5292446-077b-4057-8f5f-99561df53fca" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="2382" height="100" alt="image" src="https://github.com/user-attachments/assets/3ea00405-aa51-4089-afc2-d69b06914845" />



egrep '(world$)' newfile 
## OUTPUT

<img width="2382" height="96" alt="image" src="https://github.com/user-attachments/assets/13eabc6d-3145-4f23-8a21-d06e70da7df9" />



egrep '(World$)' newfile 
## OUTPUT

<img width="2382" height="96" alt="image" src="https://github.com/user-attachments/assets/11efa7bc-13b7-4e11-ab98-ae4876946407" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="2382" height="192" alt="image" src="https://github.com/user-attachments/assets/f260344a-b8a0-4324-b37a-ca2feef0e350" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="2382" height="102" alt="image" src="https://github.com/user-attachments/assets/d690cd86-e874-4db9-819c-7bed3d442df7" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="2382" height="102" alt="image" src="https://github.com/user-attachments/assets/205266f7-1f80-4203-a495-9fc397c51666" />



egrep 'Linux.*World' newfile 
## OUTPUT

<img width="2382" height="102" alt="image" src="https://github.com/user-attachments/assets/5908c387-9320-412c-8bb9-af603a776374" />



egrep l{2} newfile
## OUTPUT

<img width="2382" height="144" alt="image" src="https://github.com/user-attachments/assets/69023557-c548-4eee-9286-0d0f3b445442" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="2382" height="186" alt="image" src="https://github.com/user-attachments/assets/80ebb09a-6d79-423c-a402-92e2207644fd" />



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


sed -n -e '3p' file23
## OUTPUT

<img width="2382" height="94" alt="image" src="https://github.com/user-attachments/assets/0b450042-f7a3-45a2-b790-d5d74d9f605f" />



sed -n -e '$p' file23
## OUTPUT

<img width="2382" height="94" alt="image" src="https://github.com/user-attachments/assets/c8278ea2-712e-4b24-940f-c15d5a35330a" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="2382" height="416" alt="image" src="https://github.com/user-attachments/assets/cfafa603-50e1-469e-862c-db0151b9edbf" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="2382" height="416" alt="image" src="https://github.com/user-attachments/assets/a2010526-12ff-4792-ad32-9b9adb6fbfef" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="2382" height="416" alt="image" src="https://github.com/user-attachments/assets/66a69197-6b39-402a-8b4d-8d7fb8617a8d" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="2382" height="282" alt="image" src="https://github.com/user-attachments/assets/126e3c17-33ff-4606-9380-b260adf75299" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="2382" height="192" alt="image" src="https://github.com/user-attachments/assets/b0a1e14c-1132-4032-8e1b-3f2cfe8d7f74" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="2382" height="148" alt="image" src="https://github.com/user-attachments/assets/c41333cf-1d63-43ff-b39e-df7f6968d895" />


seq 10 
## OUTPUT

<img width="2382" height="512" alt="image" src="https://github.com/user-attachments/assets/691fb0e9-dc47-4ddc-a13b-cfb102d22423" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="2382" height="188" alt="image" src="https://github.com/user-attachments/assets/0037783d-8f88-4225-a21d-04e20222b518" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="2382" height="94" alt="image" src="https://github.com/user-attachments/assets/1fbe4523-45e0-4561-870e-2e2b5cc0c09d" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="2382" height="94" alt="image" src="https://github.com/user-attachments/assets/cbd61005-6321-4221-b6f4-275da1c5303f" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="2382" height="94" alt="image" src="https://github.com/user-attachments/assets/11ae1218-26dd-4241-bb28-38f7ee645b82" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="2382" height="94" alt="image" src="https://github.com/user-attachments/assets/d49c0357-7de6-4b05-9833-7378ab43b006" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="2382" height="94" alt="image" src="https://github.com/user-attachments/assets/75e9bb9a-5db8-45e6-b07a-6c4cf96c2f51" />


sed -n '2,4{s/$/*/;p}' file23

<img width="2382" height="94" alt="image" src="https://github.com/user-attachments/assets/b113bdce-e5f4-4dc0-8cee-347b40bbdd42" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="2382" height="272" alt="image" src="https://github.com/user-attachments/assets/98471c1b-d3af-494f-8e39-c04d08a6951a" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="2382" height="272" alt="image" src="https://github.com/user-attachments/assets/638cdb7a-7c70-4ae6-8dd3-9fc3fa81a7be" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="2440" height="412" alt="image" src="https://github.com/user-attachments/assets/053a8c3d-a83e-4de4-8856-83093e582430" />


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

<img width="2524" height="186" alt="image" src="https://github.com/user-attachments/assets/6287f29d-d92f-4cfe-bd9d-40d983436487" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="2524" height="186" alt="image" src="https://github.com/user-attachments/assets/78fcdcef-2c36-4f09-88d2-d3cb1142e856" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="1966" height="2358" alt="image" src="https://github.com/user-attachments/assets/26fb1bac-2140-47b8-bcf1-20d4fb7c9b34" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1966" height="2358" alt="image" src="https://github.com/user-attachments/assets/bb30a398-f4a9-45e1-9a67-b54a734f07e3" />


tar -xvf backup.tar
## OUTPUT

<img width="1966" height="2358" alt="image" src="https://github.com/user-attachments/assets/5f16ff5c-1d12-4471-8695-499914fca83b" />

gzip backup.tar

ls .gz
## OUTPUT


gunzip backup.tar.gz
## OUTPUT
<img width="1966" height="84" alt="image" src="https://github.com/user-attachments/assets/f6480c92-3e74-4707-9f90-834287adba2f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="2606" height="316" alt="image" src="https://github.com/user-attachments/assets/46438f6b-df58-4a4b-be8b-7fc454850d9d" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="2606" height="208" alt="image" src="https://github.com/user-attachments/assets/17031096-ec27-4b55-890d-c903c83ef790" />


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

<img width="2606" height="758" alt="image" src="https://github.com/user-attachments/assets/e49c55af-24ef-4db4-812d-984cb35e9bcf" />

 
ls file1
## OUTPUT

<img width="2606" height="104" alt="image" src="https://github.com/user-attachments/assets/03c9274a-65ee-489a-8174-5c609b1f25b4" />

echo $?
## OUTPUT 


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="2606" height="104" alt="image" src="https://github.com/user-attachments/assets/a6262b05-6dd4-4bee-8842-590eb398a8fa" />

abcd
 
echo $?
 ## OUTPUT

<img width="2606" height="104" alt="image" src="https://github.com/user-attachments/assets/3e4b9d6b-1b8d-43bf-ba67-ce2ba6544a7d" />

 
# mis-using string comparisons

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

<img width="2606" height="562" alt="image" src="https://github.com/user-attachments/assets/f3de0dec-9d62-48fe-bfe1-4fad52078a80" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="2606" height="84" alt="image" src="https://github.com/user-attachments/assets/08f22b3c-e328-4c86-b2ce-6361f57eb459" />


# check file ownership
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

./ifnested.sh 
## OUTPUT

<img width="2606" height="176" alt="image" src="https://github.com/user-attachments/assets/3466860b-e092-4d9a-883b-0c9c7107a2e8" />


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
 
$ ./iftest.sh 
##OUTPUT

<img width="2606" height="176" alt="image" src="https://github.com/user-attachments/assets/7072cb6f-467f-48de-af60-233e38a2633a" />

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

<img width="2606" height="176" alt="image" src="https://github.com/user-attachments/assets/f41bf52c-43bb-45d7-98d6-6b0e646fb786" />

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

<img width="2606" height="138" alt="image" src="https://github.com/user-attachments/assets/cf9c6ee6-8b67-4a4e-bbea-1ed9a5c3c88b" />

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

<img width="2606" height="138" alt="image" src="https://github.com/user-attachments/assets/a880bc48-6372-41f4-9eaa-c2d9aea36270" />


# using the case command
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

 <img width="2606" height="138" alt="image" src="https://github.com/user-attachments/assets/9cc8085b-d4c0-46dc-817b-46212bd02e81" />

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
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh

 <img width="2606" height="484" alt="image" src="https://github.com/user-attachments/assets/3eb833d6-72c7-43b0-ab9d-1184c7c2b711" />

 
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
 
 <img width="2606" height="222" alt="image" src="https://github.com/user-attachments/assets/7a0684a3-f611-47cd-9456-7f9fd4980064" />

 
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
 <img width="2606" height="352" alt="image" src="https://github.com/user-attachments/assets/e4228d8a-4cd0-43eb-8d38-a1f4692d9f85" />

 
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

 <img width="2606" height="218" alt="image" src="https://github.com/user-attachments/assets/14dc8a12-0bd3-47ef-b2e2-a437cf1d1cbd" />

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
 
$ ./forin2.sh 

 <img width="2606" height="218" alt="image" src="https://github.com/user-attachments/assets/72cc0882-8753-49d9-b281-f740912d058a" />

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
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
$ chmod 755 forin1.sh

## OUTPUT
<img width="2606" height="354" alt="image" src="https://github.com/user-attachments/assets/392941ad-dcf3-4f7c-a4e4-fe89b38ed424" />



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

<img width="2606" height="658" alt="image" src="https://github.com/user-attachments/assets/df05157d-7375-4f02-a29b-a2d7fd963069" />


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

<img width="2606" height="310" alt="image" src="https://github.com/user-attachments/assets/146a2bc7-227c-423c-80dd-2ccc63271cfa" />


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

<img width="2606" height="310" alt="image" src="https://github.com/user-attachments/assets/1fa4beaf-57bb-41d7-8326-ab22649e6f27" />

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
 
<img width="2606" height="616" alt="image" src="https://github.com/user-attachments/assets/56becd50-2d82-4f1c-b382-5174b5532284" />

 
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
<img width="2606" height="186" alt="image" src="https://github.com/user-attachments/assets/e2c0a574-9295-41fb-ae3f-8ef6648fa064" />

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT

 <img width="2606" height="312" alt="image" src="https://github.com/user-attachments/assets/1f09067d-8a6e-4334-8868-388dff8191af" />

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

<img width="2606" height="182" alt="image" src="https://github.com/user-attachments/assets/7ce24c48-7169-4c1f-80d2-4d6efb7ff8eb" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 

 <img width="2606" height="182" alt="image" src="https://github.com/user-attachments/assets/99578425-327f-4fc6-91a7-97086722e286" />

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
 ./funcex.sh 

 <img width="2606" height="134" alt="image" src="https://github.com/user-attachments/assets/4319c8d3-e7e4-4b65-a4ef-da10c2146556" />

 ./funcex.sh 1 2
<img width="2606" height="96" alt="image" src="https://github.com/user-attachments/assets/be8ae202-0179-4757-9e5e-658807e61150" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3

 <img width="2606" height="224" alt="image" src="https://github.com/user-attachments/assets/cdac90db-8324-4843-9d86-fdda68c2cd2e" />

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
$ ./argshift.sh 1 2 3


 <img width="2606" height="224" alt="image" src="https://github.com/user-attachments/assets/8c257b52-2695-4a0a-b132-487236641234" />

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
 
 <img width="2606" height="700" alt="image" src="https://github.com/user-attachments/assets/f2f5011a-b94b-4acb-a7e0-74e4ddde60de" />

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
awk -f nc.awk data.dat
## OUTPUT 

 <img width="2606" height="618" alt="image" src="https://github.com/user-attachments/assets/f68bad3e-bbc2-4f32-89b7-3e4cae986d40" />

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

<img width="2606" height="218" alt="image" src="https://github.com/user-attachments/assets/2d2abff5-7d8b-4cf4-819d-22d53659fa5e" />


# RESULT:
The Commands are executed successfully.
