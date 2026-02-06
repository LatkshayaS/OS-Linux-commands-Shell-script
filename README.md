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

<img width="733" height="275" alt="image" src="https://github.com/user-attachments/assets/15f3a37f-9cd1-4b4c-a2bf-7c010b1e885c" />


cat < file2
## OUTPUT
<img width="994" height="237" alt="image" src="https://github.com/user-attachments/assets/3934cd58-59e1-4621-b99a-7341b086d534" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="421" height="61" alt="image" src="https://github.com/user-attachments/assets/701fc221-6c0c-477e-a6b7-2fcee5afd450" />

comm file1 file2
 ## OUTPUT

 <img width="1156" height="432" alt="image" src="https://github.com/user-attachments/assets/27b196f0-6c97-44db-8f22-5e44a2ef1f3a" />

diff file1 file2
## OUTPUT

<img width="1147" height="407" alt="image" src="https://github.com/user-attachments/assets/19421637-ac5f-444a-bba9-cf49ca832b4e" />

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

<img width="870" height="162" alt="image" src="https://github.com/user-attachments/assets/3620562b-349d-422b-aaa2-f79573ec2579" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="616" height="181" alt="image" src="https://github.com/user-attachments/assets/4669b28d-9b81-4f8d-b8f8-95d65a2a1001" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="902" height="185" alt="image" src="https://github.com/user-attachments/assets/59aab742-9735-454e-9262-311522643ed9" />


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

<img width="944" height="78" alt="image" src="https://github.com/user-attachments/assets/b8db4fc7-38a8-4b3a-8497-41d88252960e" />


grep hello newfile 
## OUTPUT


<img width="969" height="69" alt="image" src="https://github.com/user-attachments/assets/5c74ac12-8445-4dca-85eb-c8483d4cabb2" />


grep -v hello newfile 
## OUTPUT

<img width="885" height="180" alt="image" src="https://github.com/user-attachments/assets/5ed974a7-6944-4fa2-8e00-ca508f5237ad" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="736" height="96" alt="image" src="https://github.com/user-attachments/assets/42a3b1e4-497e-409c-b9cf-8fed3b057b8e" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="619" height="69" alt="image" src="https://github.com/user-attachments/assets/04503f92-f4bd-4194-9508-89403a225598" />



grep -R ubuntu /etc
## OUTPUT

<img width="554" height="95" alt="image" src="https://github.com/user-attachments/assets/7707097b-2369-453e-9f84-b0e06f1d46ed" />


grep -w -n world newfile   
## OUTPUT
<img width="1182" height="930" alt="image" src="https://github.com/user-attachments/assets/b4159246-6fce-4959-a218-d087a4777def" />


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

<img width="710" height="92" alt="image" src="https://github.com/user-attachments/assets/4aee82b7-bb51-488d-81ee-fd87ed9fd8e7" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="542" height="91" alt="image" src="https://github.com/user-attachments/assets/6210d560-8052-4bba-b434-b64eec3f92b8" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="789" height="92" alt="image" src="https://github.com/user-attachments/assets/8807c71a-8d29-4027-a28b-f120028e547e" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="700" height="76" alt="image" src="https://github.com/user-attachments/assets/0ba18e20-c6c6-4116-94e7-87d2444cef44" />


egrep '(world$)' newfile 
## OUTPUT

<img width="645" height="95" alt="image" src="https://github.com/user-attachments/assets/70b8f724-e595-4fd4-b7e1-d46cabe4dae4" />


egrep '(World$)' newfile 
## OUTPUT
<img width="645" height="95" alt="image" src="https://github.com/user-attachments/assets/173e565f-fb2e-4e6c-94fd-b776fecc61f2" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="854" height="118" alt="image" src="https://github.com/user-attachments/assets/25ced1b1-50db-4ee5-9f0c-d3dfe28d9812" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="864" height="74" alt="image" src="https://github.com/user-attachments/assets/4b0eb43d-d850-496d-8348-674ba4c8225e" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="680" height="72" alt="image" src="https://github.com/user-attachments/assets/e643c8b5-1b04-438f-9c61-df3758e871ac" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="726" height="68" alt="image" src="https://github.com/user-attachments/assets/0ac5450c-ca9a-4433-82ff-fd4315211374" />


egrep l{2} newfile
## OUTPUT

<img width="768" height="96" alt="image" src="https://github.com/user-attachments/assets/d118e817-324b-4b83-975e-cb4affcfd5ed" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="769" height="120" alt="image" src="https://github.com/user-attachments/assets/9c015f35-7f1c-477b-b661-237d43c501be" />


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

<img width="952" height="70" alt="image" src="https://github.com/user-attachments/assets/cc20e833-b1d0-4357-8f04-2f3f2ac099db" />


sed -n -e '$p' file23
## OUTPUT


<img width="781" height="72" alt="image" src="https://github.com/user-attachments/assets/80bd75f1-adfe-4b21-8a42-a3fc5e6b8d42" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="665" height="96" alt="image" src="https://github.com/user-attachments/assets/588b37e0-e34d-4b3f-84d5-45fbb4f1371d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT




<img width="770" height="374" alt="image" src="https://github.com/user-attachments/assets/35c8e927-7ab5-4b14-93f3-d948fc5a5b0b" />


<img width="859" height="435" alt="image" src="https://github.com/user-attachments/assets/fddfdd4c-e341-4cc2-a7aa-8c12a914b034" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="762" height="182" alt="image" src="https://github.com/user-attachments/assets/9f8d2e7d-6597-49eb-8d9a-529efb7ccf05" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="730" height="415" alt="image" src="https://github.com/user-attachments/assets/7c9b04e6-f017-4a5c-a0aa-61a12b8be57e" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="666" height="169" alt="image" src="https://github.com/user-attachments/assets/ab22a748-d4bf-479e-8e6a-070fb39930a5" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="835" height="113" alt="image" src="https://github.com/user-attachments/assets/5dfd93bd-34dc-4122-8cef-8f77241b2cf4" />


seq 10 
## OUTPUT


<img width="779" height="273" alt="image" src="https://github.com/user-attachments/assets/f53a1cb3-4a69-483f-b398-a509aa761ed8" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="942" height="122" alt="image" src="https://github.com/user-attachments/assets/d3f80fbd-045e-4531-bb38-cbec64583963" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="764" height="117" alt="image" src="https://github.com/user-attachments/assets/5d322684-0a2a-4aed-9f3e-078a6ae6c3af" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="679" height="139" alt="image" src="https://github.com/user-attachments/assets/6539f3fc-a24b-43c2-8ea6-0fec6e2d3485" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="623" height="110" alt="image" src="https://github.com/user-attachments/assets/bd55cc9b-5a88-4ffb-8d1b-f5e5965798cf" />


seq 10 | sed '2,9c hello'
## OUTPUT


<img width="839" height="119" alt="image" src="https://github.com/user-attachments/assets/d231f17d-a16f-44ef-89a8-8953f5fa2bf2" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="1003" height="112" alt="image" src="https://github.com/user-attachments/assets/4ca8c103-7984-4038-bc33-accbe1865c1f" />


sed -n '2,4{s/$/*/;p}' file23


<img width="912" height="113" alt="image" src="https://github.com/user-attachments/assets/ed49c632-91fa-48a4-b4b7-53a3472c5849" />

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

<img width="732" height="516" alt="image" src="https://github.com/user-attachments/assets/2e1b5570-fef5-456f-a1c5-b9dfc39eafbe" />


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


<img width="812" height="567" alt="image" src="https://github.com/user-attachments/assets/9229f511-da40-40d4-9f49-63b004e7ce3a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="882" height="420" alt="image" src="https://github.com/user-attachments/assets/86c510fb-5bb8-4e30-8504-e693466fa47f" />

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


<img width="766" height="185" alt="image" src="https://github.com/user-attachments/assets/d603f3c6-da7b-4555-aef2-0cfbfb15c19a" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT




#Backup commands
tar -cvf backup.tar *
## OUTPUT



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="989" height="632" alt="image" src="https://github.com/user-attachments/assets/0e2c1473-aac1-4ab8-9497-d56d827c3925" />


tar -xvf backup.tar
## OUTPUT

<img width="989" height="632" alt="image" src="https://github.com/user-attachments/assets/2a478d0c-0442-4916-89d9-73daf2c2bd10" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="741" height="95" alt="image" src="https://github.com/user-attachments/assets/867deb54-0ef0-4acf-8e2a-2985a87ab781" />

gunzip backup.tar.gz
## OUTPUT

<img width="1169" height="118" alt="image" src="https://github.com/user-attachments/assets/c90e85ee-8879-447b-88f8-16ed794abb78" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="872" height="233" alt="image" src="https://github.com/user-attachments/assets/054952fd-1cee-4ed4-a748-36dffe0b6735" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


<img width="675" height="364" alt="image" src="https://github.com/user-attachments/assets/40ebeb65-83cc-4030-8cd2-47432d7c0019" />

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


 <img width="948" height="66" alt="image" src="https://github.com/user-attachments/assets/dc450320-1de6-4a2b-b9ba-7475259cef88" />

ls file1
## OUTPUT


echo $?
## OUTPUT 

<img width="790" height="77" alt="image" src="https://github.com/user-attachments/assets/8cbc6525-f24e-4bef-a878-9a5d7b8236c8" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="638" height="71" alt="image" src="https://github.com/user-attachments/assets/6bf0e2a7-00f8-4e96-abce-d5819e1c6e31" />

abcd
 
echo $?
 ## OUTPUT


<img width="1159" height="925" alt="image" src="https://github.com/user-attachments/assets/e7962592-c883-42a6-b8d2-02451edd310f" />

 
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


<img width="790" height="77" alt="image" src="https://github.com/user-attachments/assets/54153bf6-f946-4d00-861e-883efa060a57" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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

<img width="1160" height="746" alt="image" src="https://github.com/user-attachments/assets/bda4dc91-d7ef-4ab5-8b3f-2eced0f5ac83" />

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


<img width="1004" height="818" alt="image" src="https://github.com/user-attachments/assets/213c750e-9744-4375-ab3b-41e3dd33b297" />


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

<img width="1157" height="928" alt="image" src="https://github.com/user-attachments/assets/e8579e31-0979-41e4-b16b-1989fc4b6494" />

<img width="1149" height="930" alt="image" src="https://github.com/user-attachments/assets/6e034a84-d1f3-415a-adcd-b4960eda56cd" />

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

<img width="1160" height="928" alt="image" src="https://github.com/user-attachments/assets/b275638a-fae6-4f19-86b2-1a4c556ff4d9" />

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

<img width="970" height="638" alt="image" src="https://github.com/user-attachments/assets/1203b60e-1270-45ab-b20e-baf1fed61104" />

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

 <img width="895" height="411" alt="image" src="https://github.com/user-attachments/assets/7123ce29-7d5a-4402-923d-9e6675c74553" />

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
 

<img width="884" height="545" alt="image" src="https://github.com/user-attachments/assets/c06ba5dd-0547-4581-8493-f6549b2d7644" />
 
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
 

 <img width="884" height="545" alt="image" src="https://github.com/user-attachments/assets/02e6d818-0033-4ab0-bb3d-6eb227e2b8a4" />

 
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

<img width="771" height="812" alt="image" src="https://github.com/user-attachments/assets/b0854b70-eff2-4fe5-8560-96316a01d40d" />
 
 
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
$ chmod 755 forin2.sh

 <img width="700" height="311" alt="image" src="https://github.com/user-attachments/assets/92b861bc-87d8-4632-ba07-43061aae6d43" />

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
$ ./forin3.sh 

<img width="1193" height="511" alt="image" src="https://github.com/user-attachments/assets/2b4ef353-b648-4082-9210-fce6a8af5c51" />


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

<img width="727" height="286" alt="image" src="https://github.com/user-attachments/assets/1f70a83a-bf8a-4e28-8115-575537196f16" />

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

<img width="1193" height="511" alt="image" src="https://github.com/user-attachments/assets/5f066047-df72-48d2-80bb-0afaa2cd9ec2" />


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

<img width="727" height="286" alt="image" src="https://github.com/user-attachments/assets/685dc24e-b65a-4538-9bb8-4e639c01dc7d" />

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

<img width="727" height="286" alt="image" src="https://github.com/user-attachments/assets/f50205d0-cefc-47bb-a8cd-6a5c9614909f" />

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

<img width="731" height="362" alt="image" src="https://github.com/user-attachments/assets/dd5d21c6-55c2-4db3-8018-3448ef397afb" />

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

 <img width="658" height="386" alt="image" src="https://github.com/user-attachments/assets/79943cd4-9794-4eb7-bf78-95dc567bff43" />

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

<img width="440" height="226" alt="image" src="https://github.com/user-attachments/assets/0d559130-ccd2-4229-b39d-c3bb5fcece5c" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="440" height="226" alt="image" src="https://github.com/user-attachments/assets/77198a12-f5eb-4abc-9499-9ca3e8ccaee5" />


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

<img width="513" height="323" alt="image" src="https://github.com/user-attachments/assets/3177d7b9-7d55-44c0-a4ea-8a1cab19578c" />

 
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

 <img width="593" height="486" alt="image" src="https://github.com/user-attachments/assets/5301c1e5-eaf8-431e-8816-c6ef7e9e402e" />

<img width="569" height="322" alt="image" src="https://github.com/user-attachments/assets/345d8222-4bee-405a-b577-39020bf0f54a" />

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

 <img width="569" height="322" alt="image" src="https://github.com/user-attachments/assets/747258fa-239d-4b80-8df1-3d20e3a63df8" />

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
 

 <img width="569" height="322" alt="image" src="https://github.com/user-attachments/assets/64d41e98-b602-4a38-afef-0dcc78e97d0d" />

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


<img width="581" height="541" alt="image" src="https://github.com/user-attachments/assets/69f9d03a-e43b-4aea-8fe4-9559b14fca6f" />

# RESULT:
The Commands are executed successfully.
