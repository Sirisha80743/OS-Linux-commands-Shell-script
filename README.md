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

<img width="247" height="165" alt="Screenshot 2025-08-11 113752" src="https://github.com/user-attachments/assets/31a31f43-5391-48c8-a4e0-dcc416529ea4" />


cat < file2
## OUTPUT

<img width="280" height="142" alt="Screenshot 2025-08-11 113809" src="https://github.com/user-attachments/assets/369a68a7-9c65-49d1-b6ad-e07137f1710b" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="358" height="85" alt="Screenshot 2025-08-11 113943" src="https://github.com/user-attachments/assets/ef2968fb-8ff3-4c58-9d8b-1a0916c820c1" />

comm file1 file2
 ## OUTPUT

 <img width="358" height="298" alt="Screenshot 2025-08-11 114614" src="https://github.com/user-attachments/assets/b43d11e7-294f-4f65-a867-fd31ef6fc1b3" />

diff file1 file2
## OUTPUT
<img width="277" height="292" alt="Screenshot 2025-08-11 114659" src="https://github.com/user-attachments/assets/dddc06a6-32fb-4ce7-a786-68cf64694b17" />


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
<img width="250" height="104" alt="image" src="https://github.com/user-attachments/assets/bb975423-321d-46a7-83fb-147eba42cf0f" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="314" height="122" alt="image" src="https://github.com/user-attachments/assets/06d3d8a9-ed2b-49af-a0fd-821c1a50beca" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="313" height="130" alt="image" src="https://github.com/user-attachments/assets/f710ccf4-5c0e-4cff-983a-27977dd50042" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
## OUTPUT

<img width="205" height="105" alt="image" src="https://github.com/user-attachments/assets/a339ecb9-bcdc-470d-9096-848b1c580f99" />

grep Hello newfile 
## OUTPUT


<img width="266" height="78" alt="image" src="https://github.com/user-attachments/assets/24679111-21c5-4343-89f6-ac32e291648f" />


grep hello newfile 
## OUTPUT

<img width="264" height="78" alt="image" src="https://github.com/user-attachments/assets/4f6c62f6-eac1-4f94-a592-a028db12654a" />




grep -v hello newfile 
## OUTPUT


<img width="301" height="69" alt="image" src="https://github.com/user-attachments/assets/11e4182f-7bfa-48ff-9b81-6cd0823d0065" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="364" height="100" alt="image" src="https://github.com/user-attachments/assets/e115f001-fa2b-4ff6-96a3-f13c05d3f87c" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="397" height="78" alt="image" src="https://github.com/user-attachments/assets/66f66aa9-df63-4ea8-8bf6-885441dae9e7" />




grep -R ubuntu /etc
## OUTPUT


<img width="1443" height="847" alt="image" src="https://github.com/user-attachments/assets/4b131b5a-7eb2-4d9a-93ec-9c0319371499" />


grep -w -n world newfile   
## OUTPUT

<img width="327" height="105" alt="image" src="https://github.com/user-attachments/assets/0e8aacc8-cff1-4cfd-b351-34b09f54229d" />


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

<img width="332" height="173" alt="image" src="https://github.com/user-attachments/assets/60fe1414-0431-4f84-9d1f-ceb82a5ed9d5" />

egrep -w 'Hello|hello' newfile 
## OUTPUT


<img width="380" height="103" alt="image" src="https://github.com/user-attachments/assets/43a63b0e-916f-4087-b0f2-999a2d46f6f4" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="359" height="98" alt="image" src="https://github.com/user-attachments/assets/df78aa13-044c-42b2-a40c-514540dfe09e" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="402" height="104" alt="image" src="https://github.com/user-attachments/assets/31cbf48f-4808-4eec-9b3a-73e648be2dfa" />




egrep '(^hello)' newfile 
## OUTPUT


,<img width="331" height="67" alt="image" src="https://github.com/user-attachments/assets/e3d738d7-ca89-4f8f-85f8-5c7877574fc3" />


egrep '(world$)' newfile 
## OUTPUT


<img width="323" height="104" alt="image" src="https://github.com/user-attachments/assets/498046e0-8d26-4a2a-81af-b3509544ae5d" />


egrep '(World$)' newfile 
## OUTPUT

<img width="333" height="81" alt="image" src="https://github.com/user-attachments/assets/12781250-933e-4485-9188-d3407a5b43b5" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="365" height="132" alt="image" src="https://github.com/user-attachments/assets/d29f239c-e916-4b8b-89e7-1bc87b4e996d" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="290" height="82" alt="image" src="https://github.com/user-attachments/assets/a243f379-00b7-41ef-888f-969f86208d4b" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="363" height="81" alt="image" src="https://github.com/user-attachments/assets/b5c75698-49c1-486d-bb46-4829c8630387" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="367" height="69" alt="image" src="https://github.com/user-attachments/assets/66c653ab-821c-4cf3-ba6c-25183dc75d88" />


egrep l{2} newfile
## OUTPUT


<img width="261" height="105" alt="image" src="https://github.com/user-attachments/assets/115e5611-aa65-4ade-bbb7-1fbb089a9b45" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="332" height="129" alt="image" src="https://github.com/user-attachments/assets/3482d10b-a1a2-4690-9264-1cae157ae64b" />


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


<img width="295" height="78" alt="image" src="https://github.com/user-attachments/assets/84426f73-a352-4f6f-adbf-3a4027f31f0f" />


sed -n -e '$p' file23
## OUTPUT

<img width="286" height="77" alt="image" src="https://github.com/user-attachments/assets/bda0b8f9-a090-47f5-ba6b-e517c79b8d4c" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="380" height="253" alt="image" src="https://github.com/user-attachments/assets/500249b9-3ee4-4ffc-9134-4d3732bf2273" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="391" height="249" alt="image" src="https://github.com/user-attachments/assets/5d3a9127-a75a-4155-8eaa-d883bc4e17f5" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="387" height="251" alt="image" src="https://github.com/user-attachments/assets/05711477-9baf-473b-aa98-13f1e058f77e" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="341" height="182" alt="image" src="https://github.com/user-attachments/assets/f0285736-ab1b-42d2-afe3-69be55b288de" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="351" height="126" alt="image" src="https://github.com/user-attachments/assets/ccbcff16-81ae-4a17-840f-0a0d61ae2874" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="397" height="110" alt="image" src="https://github.com/user-attachments/assets/09a9c26d-6d26-441d-a77c-948ce51205b9" />


seq 10 
## OUTPUT

<img width="274" height="303" alt="image" src="https://github.com/user-attachments/assets/58a67e7d-cd9c-47d5-bd9c-2e08d240e00e" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="297" height="134" alt="image" src="https://github.com/user-attachments/assets/5c349f5d-a221-4976-ab54-8fdca023db0c" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="321" height="124" alt="image" src="https://github.com/user-attachments/assets/34ffd255-c0be-48bb-91e5-1051bd2ae6f4" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="293" height="154" alt="image" src="https://github.com/user-attachments/assets/8baf5c52-d6b5-44e3-a30c-3f60c6fa1c32" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="307" height="126" alt="image" src="https://github.com/user-attachments/assets/4a2f8e8a-e4f4-4525-9a30-69c8c373aa3c" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="332" height="129" alt="image" src="https://github.com/user-attachments/assets/8e4076ca-9304-403f-8e16-da211614d528" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="378" height="134" alt="image" src="https://github.com/user-attachments/assets/efafb065-3466-4032-b133-e9853fb0545b" />


sed -n '2,4{s/$/*/;p}' file23

<img width="371" height="126" alt="image" src="https://github.com/user-attachments/assets/53ae74fc-a6f2-4bc0-9b36-e8b067d6b4cd" />

#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

<img width="314" height="175" alt="image" src="https://github.com/user-attachments/assets/9a0d5e87-6103-4e02-af16-1861d44348c3" />

sort file21
## OUTPUT

<img width="310" height="177" alt="image" src="https://github.com/user-attachments/assets/0aca2388-cc1b-4c8b-b5ce-1fe8426bbea4" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

<img width="320" height="203" alt="image" src="https://github.com/user-attachments/assets/b0164062-bb3f-4816-a837-ea2895a7c897" />


uniq file22
## OUTPUT

<img width="323" height="177" alt="image" src="https://github.com/user-attachments/assets/ddb1477e-03ba-43a1-90f9-bb1a40aa36e8" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="426" height="253" alt="image" src="https://github.com/user-attachments/assets/70f6ae0c-c454-45f8-afc5-c009e3076d47" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```

<img width="271" height="127" alt="image" src="https://github.com/user-attachments/assets/7534e144-f8fa-44d0-b2e0-21e571ca9afa" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="347" height="124" alt="image" src="https://github.com/user-attachments/assets/c8f13bc4-099e-4ea5-b437-05a770b52269" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="471" height="132" alt="image" src="https://github.com/user-attachments/assets/07a5b52f-9f36-444c-b68a-278c9299f993" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="297" height="253" alt="image" src="https://github.com/user-attachments/assets/d8def213-115d-429e-b108-7494dc80f629" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="631" height="305" alt="image" src="https://github.com/user-attachments/assets/0a958dbd-7a04-4b64-aafa-4d383a511cd8" />



tar -xvf backup.tar
## OUTPUT

<img width="393" height="299" alt="image" src="https://github.com/user-attachments/assets/cc90fdfe-bd8b-4491-a0bd-a25d9a5c978b" />

gzip backup.tar

ls .gz
## OUTPUT

<img width="355" height="79" alt="image" src="https://github.com/user-attachments/assets/86385166-7dd3-4b91-9c0e-d5a6728a27c7" />
 
gunzip backup.tar.gz
ls
## OUTPUT

<img width="491" height="114" alt="image" src="https://github.com/user-attachments/assets/79d64e81-0c41-476c-98f6-08dc38bef47b" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="685" height="181" alt="image" src="https://github.com/user-attachments/assets/e8ee1048-402f-4415-8027-b82d8d585949" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="279" height="132" alt="image" src="https://github.com/user-attachments/assets/3d6aac6f-3c2b-4402-a225-0318cd889bf1" />

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
## OUTPUT
<img width="368" height="340" alt="image" src="https://github.com/user-attachments/assets/08ffbf0e-fc06-4f08-97e0-320e7bfcce9d" />

chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

<img width="611" height="455" alt="image" src="https://github.com/user-attachments/assets/0f57a71c-cac6-4c38-9e53-e32e2d00a372" />
 
ls file1
## OUTPUT

<img width="259" height="81" alt="image" src="https://github.com/user-attachments/assets/f4287aa6-30ae-480f-bc07-1b6bfabb6706" />

echo $?
## OUTPUT 

<img width="250" height="91" alt="image" src="https://github.com/user-attachments/assets/980b3bc4-74fc-4910-9729-3be175e4d57e" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="285" height="76" alt="image" src="https://github.com/user-attachments/assets/c3c93a31-ad0e-4be1-9512-ba02001ac00b" />
 
abcd
 
echo $?
 ## OUTPUT

<img width="295" height="84" alt="image" src="https://github.com/user-attachments/assets/b74ab68c-d6fd-4b7c-82eb-22a7084d6a5e" />

 
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
## OUTPUT

<img width="372" height="283" alt="image" src="https://github.com/user-attachments/assets/9859c5f7-d415-4e3e-8c3b-8a62660211b1" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="624" height="106" alt="image" src="https://github.com/user-attachments/assets/bfcf911a-bc94-4702-9a1c-801c6e220734" />

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
## OUTPUT

<img width="614" height="230" alt="image" src="https://github.com/user-attachments/assets/3e482faa-3134-4a4b-8b89-a9b5ec0dfb28" />

./psswdperm.sh
## OUTPUT

<img width="410" height="82" alt="image" src="https://github.com/user-attachments/assets/e04f0a39-55b6-4618-9e2e-d56ea543ba77" />

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
## OUTPUT

<img width="465" height="473" alt="image" src="https://github.com/user-attachments/assets/554d13f9-e771-4f24-9965-cbb0b8c172d5" />

./ifnested.sh 
## OUTPUT

<img width="418" height="83" alt="image" src="https://github.com/user-attachments/assets/210b42c3-4292-4641-bb9e-a3213f6e88f1" />


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
## OUTPUT

<img width="486" height="370" alt="image" src="https://github.com/user-attachments/assets/757c31f6-edc5-42f3-bedb-5bb188465420" />

$chmod 755 iftest.sh
 
$./iftest.sh 
## OUTPUT

<img width="610" height="182" alt="image" src="https://github.com/user-attachments/assets/ae480a4e-2ccd-4a89-910f-19e601c62ecd" />

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
## OUTPUT
<img width="470" height="472" alt="image" src="https://github.com/user-attachments/assets/33957b84-18c8-412b-b296-f2b7b2cbae1d" />

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 

## OUTPUT
<img width="631" height="209" alt="image" src="https://github.com/user-attachments/assets/47c144d5-be10-47f6-bf1c-12ce926bc615" />

# looking for a possible value using elif
cat > elifcheck.sh 
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

<img width="640" height="148" alt="image" src="https://github.com/user-attachments/assets/ffd6b431-d671-4d9b-9809-4c0cf2e5be3f" />

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

<img width="642" height="151" alt="image" src="https://github.com/user-attachments/assets/cfc7a40e-2d98-4b9d-a68f-7776bd577799" />

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
## OUTPUT

<img width="336" height="123" alt="image" src="https://github.com/user-attachments/assets/416cac6f-4064-4c8d-8ad9-25f3c2fb11f1" />

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
 
## OUTPUT



cat > untiltest.sh 
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
$ ./untiltest.sh

## OUTPUT

<img width="321" height="206" alt="image" src="https://github.com/user-attachments/assets/4885d11f-d88c-49a3-802c-604fbc1c9eae" />
 
cat > forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
$ ./forin1.sh

## OUTPUT

<img width="606" height="301" alt="image" src="https://github.com/user-attachments/assets/67e410e1-046e-4444-894d-560d2fa8c931" />

 
cat > forin2.sh 
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

## OUTPUT

<img width="289" height="175" alt="image" src="https://github.com/user-attachments/assets/b8fa45fb-9c30-4b58-b3e0-a8dd283b494a" />
 
cat > forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh
$ ./forin3.sh 

## OUTPUT

<img width="280" height="238" alt="image" src="https://github.com/user-attachments/assets/6d12dac0-1e0f-4341-9fb8-f9e094aa4b39" />

cat > forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh
$ ./forin1.sh 

## OUTPUT
<img width="322" height="245" alt="image" src="https://github.com/user-attachments/assets/8c071d11-feca-476c-90f2-eaa46dd93a46" />

cat > forinfile.sh 
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

 
 ./funcex.sh 1 2

 
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


# RESULT:
The Commands are executed successfully.
