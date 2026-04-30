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
<img width="953" height="165" alt="374ddc3d-44e2-4017-9d1f-b5aeecf50e26" src="https://github.com/user-attachments/assets/56987898-f49b-4532-a76a-9a5493867c39" />
# OUTPUT



cat < file2
## OUTPUT


<img width="960" height="529" alt="388afb35-84b8-4d17-a11c-f52ed03e0d27" src="https://github.com/user-attachments/assets/c6e0d051-bbc2-4980-a7c5-43791a8b350a" />
<img width="982" height="167" alt="68ea6ff4-d07b-40e4-8ef7-87ed2bd8ae0b" src="https://github.com/user-attachments/assets/298b9982-188a-45d1-be57-da7604957644" />
 Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT

 
diff file1 file2
## OUTPUT


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



<img width="960" height="529" alt="388afb35-84b8-4d17-a11c-f52ed03e0d27" src="https://github.com/user-attachments/assets/c0e65fde-7747-43f2-932f-118d52f47318" />
cut -d "|" -f 1 file22
## OUTPUT


<img width="986" height="421" alt="4554ac73-feae-4513-8562-73564da9b55e" src="https://github.com/user-attachments/assets/09f18f28-4752-422d-827e-66a73b240246" />
cut -d "|" -f 2 file22
## OUTPUT

<img width="946" height="468" alt="8cb2c01a-666b-4c1c-864e-c27cc972c08c" src="https://github.com/user-attachments/assets/b289138e-fd6a-4aae-8d79-7081f1d67853" />
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

<img width="1005" height="167" alt="WhatsApp Image 2026-04-30 at 10 15 28" src="https://github.com/user-attachments/assets/377be1b7-a689-4f86-8987-b6c036a6cc4b" />
grep hello newfile 
## OUTPUT



<img width="984" height="105" alt="dfface50-81fb-476b-9acd-cb90bbbf71d0" src="https://github.com/user-attachments/assets/7afee1ca-23e8-42f0-a24c-d455a30d559d" />
grep -v hello newfile 
## OUTPUT

<img width="972" height="117" alt="3c9ec186-a854-4d3e-bfc6-706e8e078a81" src="https://github.com/user-attachments/assets/ca890606-2e0c-4271-a187-2c18d449ff23" />
cat newfile | grep -i "hello"
## OUTPUT



<img width="941" height="100" alt="60a564c1-5269-4d33-b457-83826e4723cb" src="https://github.com/user-attachments/assets/13cec989-936c-49a0-a35c-222faf7118de" />
cat newfile | grep -i -c "hello"
## OUTPUT



<img width="1080" height="100" alt="0a47b105-83ce-46f8-a084-d71badd1452f" src="https://github.com/user-attachments/assets/0433ab15-8350-47f0-9ac1-fb5cd82a0499" />
grep -R ubuntu /etc
## OUTPUT


<img width="987" height="112" alt="aab236c1-e832-4f68-9328-3567445cc779" src="https://github.com/user-attachments/assets/d0a1aac0-6f66-4952-9bd3-abfe2aa34328" />
grep -w -n world newfile   
## OUTPUT

<img width="982" height="438" alt="d50faa56-cc5c-4584-977b-6efd4781cb3c" src="https://github.com/user-attachments/assets/7ae339ae-6c8e-474c-831e-309203232127" />
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

<img width="990" height="128" alt="90738eab-9213-4a43-8278-eff6e1685dba" src="https://github.com/user-attachments/assets/e95fd224-6ec3-4221-a04e-09cd7df9f2b7" />
egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="1001" height="99" alt="b8359706-1a33-45f4-95db-84255c2dea5d" src="https://github.com/user-attachments/assets/81a46eb3-2280-4bd8-b62d-bfd8f867803c" />
egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT



<img width="981" height="113" alt="e4c7b48d-8924-4787-9eb1-2013672c25d9" src="https://github.com/user-attachments/assets/453b7b2a-1975-4956-a954-2a1ef2a19ad4" />
egrep '(^hello)' newfile 
## OUTPUT


<img width="973" height="145" alt="22bb26ca-ff4d-4c35-8bf9-2ab9c546217b" src="https://github.com/user-attachments/assets/c2eaaa31-ca83-4bbb-88df-3d216964ec43" />
egrep '(world$)' newfile 
## OUTPUT

<img width="973" height="100" alt="f7c0727e-2580-43bc-9642-7d5f26000136" src="https://github.com/user-attachments/assets/cc743361-3248-4a73-99d5-b9dabb3da937" />
egrep '(World$)' newfile 
## OUTPUT

<img width="973" height="145" alt="22bb26ca-ff4d-4c35-8bf9-2ab9c546217b" src="https://github.com/user-attachments/assets/4f92ffb9-d8bd-46be-a675-bc89cff14f27" />

egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="971" height="100" alt="afc98f0d-392c-4e2f-a620-101cda844b14" src="https://github.com/user-attachments/assets/f138b5e7-6b3c-4dbb-8d24-ac049643a88b" />
egrep '[1-9]' newfile 
## OUTPUT



<img width="1012" height="100" alt="6c0ec9fa-6936-46d9-9a1d-e1ce54bf8861" src="https://github.com/user-attachments/assets/3bea5f27-3333-484a-863b-7541344cfae8" />
egrep 'Linux.*world' newfile 
## OUTPUT

<img width="942" height="100" alt="cc12bb88-1adc-4960-b3c8-9c5b96f9fb87" src="https://github.com/user-attachments/assets/adfa5999-a1d0-403b-af14-cb8ae7a3efcd" />
egrep 'Linux.*World' newfile 
## OUTPUT

<img width="942" height="100" alt="cc12bb88-1adc-4960-b3c8-9c5b96f9fb87" src="https://github.com/user-attachments/assets/b238ba42-d64f-4cfa-9c03-7791781bbdbc" />

egrep l{2} newfile
## OUTPUT


<img width="959" height="100" alt="c1d9b1e5-595b-4797-8c5b-61e0ca815e2e" src="https://github.com/user-attachments/assets/a59b1c07-912f-4296-a929-a313f640f03a" />
egrep 's{1,2}' newfile
## OUTPUT 

<img width="992" height="342" alt="68ff8cef-d8b6-42b1-bb37-f000d267aa58" src="https://github.com/user-attachments/assets/dc1b0269-4d59-4048-8472-281864442a38" />
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

<img width="959" height="100" alt="c1d9b1e5-595b-4797-8c5b-61e0ca815e2e" src="https://github.com/user-attachments/assets/6863636e-efb7-4ba2-b29b-5babcfb4996c" />
sed -n -e '3p' file23
## OUTPUT


<img width="985" height="274" alt="a032af4d-0e58-45d1-b957-a6f864a112ee" src="https://github.com/user-attachments/assets/55a58f6b-e2a7-4d96-b0fa-011d5fc3f164" />
sed -n -e '$p' file23
## OUTPUT


<img width="985" height="274" alt="a032af4d-0e58-45d1-b957-a6f864a112ee" src="https://github.com/user-attachments/assets/181b33e0-d3c4-469c-9d30-5130a01a3be3" />
sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="999" height="268" alt="21c07dfb-21eb-4276-870b-8d2bb2019b39" src="https://github.com/user-attachments/assets/93889604-e706-4df1-9f9a-a1a3f99fd981" />
sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="989" height="272" alt="c68fa375-d859-4ec6-bfe1-567c69d87f3b" src="https://github.com/user-attachments/assets/56f0c539-961d-4dfa-852c-966251e2c8fc" />
sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="989" height="272" alt="c68fa375-d859-4ec6-bfe1-567c69d87f3b" src="https://github.com/user-attachments/assets/e55357a3-0e9e-48ea-a0bb-9adb08858a05" />
sed -n -e '1,5p' file23
## OUTPUT


<img width="997" height="201" alt="39e94f1d-bd1f-4bb4-ae01-5b312b3e31c5" src="https://github.com/user-attachments/assets/e37deecb-2475-428e-a7df-c985415de0ef" />
sed -n -e '2,/Joe/p' file23
## OUTPUT



<img width="970" height="100" alt="ae011576-a7cf-4bd8-a578-acd106542bfb" src="https://github.com/user-attachments/assets/c5bcc332-1e1b-41f0-ab12-f8e33b34a0ab" />
sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



<img width="970" height="319" alt="218da50d-e880-4a5d-a9bb-193c4918cf3e" src="https://github.com/user-attachments/assets/68f1ecfb-8a47-4cd9-ab5b-8f6e610dfa1a" />
seq 10 
## OUTPUT


<img width="988" height="139" alt="e030190c-d87c-4567-bf34-be55398b2f27" src="https://github.com/user-attachments/assets/8140ac75-d989-4804-bafe-56835f31b78a" />
seq 10 | sed -n '4,6p'
## OUTPUT


<img width="976" height="163" alt="3842bd22-70d5-4989-b1cf-17e4f5fa8209" src="https://github.com/user-attachments/assets/7a510a51-c615-4963-86e3-df6383ff1478" />
seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="989" height="177" alt="516e526d-4dd2-4ba2-b196-89ea41e7b7e5" src="https://github.com/user-attachments/assets/ceb61a1a-eb10-40f9-90e5-7489c7ab3e79" />
seq 3 | sed '2a hello'
## OUTPUT


<img width="998" height="140" alt="6febc553-1dea-4b41-a42c-99273affd176" src="https://github.com/user-attachments/assets/39e5f818-3155-4566-a903-4625a8adfd97" />
seq 2 | sed '2i hello'
## OUTPUT

<img width="993" height="137" alt="1a81c6af-1ef1-4b5f-8f7e-847a58301688" src="https://github.com/user-attachments/assets/4d377551-4851-436b-b475-da533f9766e4" />
seq 10 | sed '2,9c hello'
## OUTPUT

<img width="984" height="149" alt="34ee8bdb-3fae-4cf3-8554-27d192449a63" src="https://github.com/user-attachments/assets/ea79edd8-a9b9-4483-85d8-e586b3c94d90" />
sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="981" height="515" alt="0f4a9f63-46b8-4dfd-8ce9-18cf5d75e98f" src="https://github.com/user-attachments/assets/1c9c549e-d8e0-420b-94bc-cd1e58e1a907" />
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
sort file21
## OUTPUT

<img width="981" height="515" alt="0f4a9f63-46b8-4dfd-8ce9-18cf5d75e98f" src="https://github.com/user-attachments/assets/a4d78afa-e495-4de6-92c0-5c4f4ffd6d78" />
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


<img width="981" height="369" alt="84d67f8c-e6f8-46d3-a506-c4fb6bc75a17" src="https://github.com/user-attachments/assets/7f485ee4-f73e-4f28-a96f-cfba475ef31f" />
#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 <img width="987" height="277" alt="9d194cd7-92bc-46c4-a7fe-99d110af542c" src="https://github.com/user-attachments/assets/2422fef2-dc61-4ca7-ba64-b4d1c6518947" />
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="981" height="394" alt="66d5ff5a-a999-45df-a762-2852a940f927" src="https://github.com/user-attachments/assets/0844bdb9-0175-4be6-99d9-70d039d805bc" />
mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="991" height="145" alt="2551d14b-91d9-4d33-824b-8019d9e0a700" src="https://github.com/user-attachments/assets/ed96e851-dc5c-4104-9079-6633371058ca" />
tar -xvf backup.tar
## OUTPUT
<img width="992" height="285" alt="49d1031f-3f72-4791-a3b0-deb9e24d1ace" src="https://github.com/user-attachments/assets/ad62d2a0-c187-48f5-b2f9-e9f52e8baa8d" />
gzip backup.tar

ls .gz
## OUTPUT
 <img width="948" height="378" alt="c656be56-dd5a-466e-865f-1cd5245e23d3" src="https://github.com/user-attachments/assets/57073be0-56d3-44ff-97a8-33563527073d" />
gunzip backup.tar.gz
## OUTPUT

 <img width="999" height="249" alt="b9830302-f65e-42ec-a32f-20238f36b02b" src="https://github.com/user-attachments/assets/ab808057-bfce-4ae3-9d8f-d68ebccb8caa" />
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="997" height="133" alt="9587868c-b0cd-4ef5-ba13-788161a92271" src="https://github.com/user-attachments/assets/d39ee1ca-d33c-4af7-bb3f-6fcbfa9c0a14" />
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="1013" height="100" alt="c609695f-c199-42ff-b6e7-cc50fa1ddeba" src="https://github.com/user-attachments/assets/51fe6d51-8113-4fbb-bd9b-2d579c2a0228" />
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

 <img width="997" height="177" alt="823f17b5-369c-401a-a487-0ed783b5553e" src="https://github.com/user-attachments/assets/dae911f7-bad4-4797-b3ec-43e65ffb24c3" />
ls file1
## OUTPUT
<img width="994" height="306" alt="abe8c356-8038-4578-ac8e-7134a8b33a4d" src="https://github.com/user-attachments/assets/fa1f0933-0884-47de-8282-29f3cf0af38e" />
echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="987" height="1112" alt="d1f70760-e6e6-4212-8d47-258d08a39f78" src="https://github.com/user-attachments/assets/c1cb31c3-f888-4e4c-b971-a6f112fe11f5" />
echo $?
## OUTPUT 
 <img width="978" height="100" alt="76e96863-395d-4021-9a03-2eb5dd207219" src="https://github.com/user-attachments/assets/84a8693f-530e-496d-8bd1-eabb458cd5a6" />
abcd
 
echo $?
 ## OUTPUT

<img width="984" height="165" alt="d5f6032b-8617-4943-b0ea-e000ef11060b" src="https://github.com/user-attachments/assets/155a8362-ada0-49d8-8451-e8373a2ed9ac" />
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


chmod 755 strcomp.sh
 <img width="982" height="652" alt="4468f107-179b-438e-a21e-1b42f769a30d" src="https://github.com/user-attachments/assets/d7b1bc1d-2d52-43c3-b4ee-87e6369c44f0" />
./strcomp.sh 
## OUTPUT

<img width="982" height="466" alt="9fa04eed-90c8-4e84-8245-ef4c702033e8" src="https://github.com/user-attachments/assets/bd72e950-7328-4ca6-8e2c-a53030131743" />
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
<img width="979" height="748" alt="3a50483f-4f4b-42f5-b638-517223424807" src="https://github.com/user-attachments/assets/9faf22d2-ee90-44ef-a5e9-678f2551b3b8" />
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


<img width="979" height="774" alt="96a713cc-c320-4b95-a7ca-97e0b79a5592" src="https://github.com/user-attachments/assets/d7e13fc1-0438-4573-9de7-aeba2ac6043c" />
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
##OUTPUT<img width="979" height="748" alt="3a50483f-4f4b-42f5-b638-517223424807" src="https://github.com/user-attachments/assets/3e3574b9-953a-4ad3-b079-df73132d6277" />

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
<img width="941" height="1095" alt="e63e2cd8-f0b6-49c2-9a2e-90c064520191" src="https://github.com/user-attachments/assets/29ae5631-cb87-44e4-ae0f-0a3920611ca9" />

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

<img width="983" height="281" alt="37aef9cb-4285-4b17-9c82-de5027e9f2bf" src="https://github.com/user-attachments/assets/34aa1770-7c28-4b1e-b272-5216593fcf47" />

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
$ ./ifcompound.sh <img width="985" height="259" alt="4d8c560f-54ac-447b-bffb-b58feb03edaf" src="https://github.com/user-attachments/assets/103a225c-db7f-4aad-8099-b45cb0bad487" />
## OUTPUT
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
esac```
<img width="968" height="422" alt="048a64cf-d15d-4c31-a0f8-8e0df4143a98" src="https://github.com/user-attachments/assets/f67580fe-3e8e-4e4d-aa99-244079a5ac5b" />
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
<img width="991" height="490" alt="42ed050c-0075-42be-a5d4-694619a18146" src="https://github.com/user-attachments/assets/7004cbe4-b3ad-4bb7-aeee-436c117fb00b" />

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
 
 
 
cat forin1.sh <img width="976" height="276" alt="63a53420-cc26-437b-86f3-02f4ae7a3a1e" src="https://github.com/user-attachments/assets/2325a9be-4965-456c-ba6c-03cb4bd731a7" />
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
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
<img width="976" height="276" alt="63a53420-cc26-437b-86f3-02f4ae7a3a1e" src="https://github.com/user-attachments/assets/bb83e87c-3ab3-45e9-8765-f04b2ee12fd3" />
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
$ ./forctype.sh <img width="991" height="631" alt="4c842bb6-e17e-48f0-be28-ad0e4f336522" src="https://github.com/user-attachments/assets/8bdf1609-b4c1-4586-aa6b-c5f1bf4aa81b" />
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
$ ./forctype1.sh <img width="979" height="447" alt="bdca0f6f-8e30-4dbc-a26a-e2b091bd42b1" src="https://github.com/user-attachments/assets/86ef36df-074d-43db-8a02-ef06788357f9" />
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
<img width="987" height="313" alt="4d351403-e889-4ce0-b9c3-2ac2d158235f" src="https://github.com/user-attachments/assets/355c2638-4f66-42b8-a1cc-0acfba77b1b7" />
## OUTPUT

 <img width="982" height="1013" alt="653e0f19-1877-437d-905f-312ba86faa34" src="https://github.com/user-attachments/assets/cb642bc4-5cd1-4a83-a145-0e8484a61656" />
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
<img width="984" height="481" alt="da9c811f-cf5d-4af7-a22d-da316da0624d" src="https://github.com/user-attachments/assets/8ed54fd1-20bc-4618-b5d6-b718aaef7f8b" />
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
 
$ ./forcontinue.sh <img width="992" height="356" alt="0ccd9845-ca3b-4ade-9081-b052069c3ff8" src="https://github.com/user-attachments/assets/8dc4c19c-2ea8-4a04-aff1-ceb59959eada" />
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
 
$ ./exread.sh <img width="1004" height="100" alt="7c56f1f2-56ea-4d9d-a3c1-7dcfe0344652" src="https://github.com/user-attachments/assets/ab7d3fc7-418f-4ac8-9290-703533a7959d" />
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
<img width="989" height="122" alt="31a19e35-ca4d-40a9-bbec-2f08e4fddf99" src="https://github.com/user-attachments/assets/5ce12eab-a168-4c4e-b5db-1497cb7184ca" />
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
<img width="985" height="502" alt="c31c40b4-b159-4530-8bb0-b948c0446103" src="https://github.com/user-attachments/assets/ccd7ef73-e121-4d20-bee9-13cee138b4dd" />## OUTPUT
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
<img width="976" height="513" alt="c273df1e-6bfe-449d-81e7-4caa5af6e5e4" src="https://github.com/user-attachments/assets/d12e6fae-d5d5-4995-a5d4-3cac2344047e" />
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
$ chmod 777 argshift.sh<img width="985" height="674" alt="8d2b1106-96b1-46f7-bcd0-3f8e71981a7d" src="https://github.com/user-attachments/assets/dd165bca-2747-4e24-963d-911c93706a74" />
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
<img width="976" height="431" alt="6ebeb260-6ca2-4fe4-b6e8-b2809309d3dd" src="https://github.com/user-attachments/assets/65ad3467-388a-4d09-abb0-3ada39983dd8" />
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
<img width="976" height="431" alt="6ebeb260-6ca2-4fe4-b6e8-b2809309d3dd" src="https://github.com/user-attachments/assets/b4f2004c-1c51-4c2e-856d-5f33061378cc" />

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

<img width="963" height="618" alt="3d20f88d-95f0-4099-8ea7-b5ca51c8a245" src="https://github.com/user-attachments/assets/43c04442-c3c6-4041-82bc-eeb8a6a14fcf" />
# RESULT:
The Commands are executed successfully.
