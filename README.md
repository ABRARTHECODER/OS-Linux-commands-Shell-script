### OS-Linux-commands-Shell-script
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
### Display the content of the file
cat < file1
## OUTPUT
<img width="363" height="123" alt="image" src="https://github.com/user-attachments/assets/611805ea-4ab3-4126-97e5-e0dc39a7a8d6" />



cat < file2
## OUTPUT
<img width="356" height="136" alt="image" src="https://github.com/user-attachments/assets/1d3db307-4ecd-45fe-acb7-632a1a5198a6" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="390" height="59" alt="image" src="https://github.com/user-attachments/assets/f7b3b53c-77a7-4e98-96fe-6552923f77f3" />

comm file1 file2
 ## OUTPUT

 <img width="410" height="181" alt="image" src="https://github.com/user-attachments/assets/ba74995b-d2a9-4a12-b6e5-c4e7e2488652" />

diff file1 file2
## OUTPUT
<img width="421" height="221" alt="image" src="https://github.com/user-attachments/assets/cdaf5137-34e4-40c7-bfb1-a5ddc2461941" />


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
<img width="421" height="70" alt="image" src="https://github.com/user-attachments/assets/283e874c-86c2-4cb1-b9dc-387930670b52" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="442" height="92" alt="image" src="https://github.com/user-attachments/assets/4fa2d73b-d685-4d12-a674-af998509e4c6" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="92" alt="image" src="https://github.com/user-attachments/assets/a70a6ec0-06e6-4d90-9199-38c4d1951f18" />


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

<img width="402" height="56" alt="image" src="https://github.com/user-attachments/assets/f17a30a7-c91d-4432-a6d6-fd825e08d262" />


grep hello newfile 
## OUTPUT

<img width="402" height="56" alt="image" src="https://github.com/user-attachments/assets/f14e0a92-bab4-4486-a7a7-e3a05d004ff6" />



grep -v hello newfile 
## OUTPUT
<img width="456" height="48" alt="image" src="https://github.com/user-attachments/assets/aa261271-e9f1-46f3-9fbe-63cd63717ee0" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="516" height="70" alt="image" src="https://github.com/user-attachments/assets/dc9b5e49-6a48-4a59-8d86-db988991550a" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="552" height="50" alt="image" src="https://github.com/user-attachments/assets/118311ce-d02a-42ff-ae85-12b1799c61ee" />




grep -R ubuntu /etc
## OUTPUT
<img width="468" height="70" alt="image" src="https://github.com/user-attachments/assets/6f489176-6ce1-4e6e-a113-75af6a99397b" />



grep -w -n world newfile   
## OUTPUT
<img width="553" height="72" alt="image" src="https://github.com/user-attachments/assets/46b0f18b-1670-4bcd-929f-80063a0fb03a" />


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
<img width="520" height="70" alt="image" src="https://github.com/user-attachments/assets/5cdc1c7b-b979-4af8-baad-9d3377959eda" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="553" height="51" alt="image" src="https://github.com/user-attachments/assets/0fd6a886-43bb-4c8d-8dde-949ce406552f" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="520" height="70" alt="image" src="https://github.com/user-attachments/assets/7e0965da-10a0-473b-ac41-a39731e8723c" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="553" height="51" alt="image" src="https://github.com/user-attachments/assets/586d9652-8049-4c3c-82b8-3d6ff0a010ca" />



egrep '(world$)' newfile 
## OUTPUT
<img width="546" height="76" alt="image" src="https://github.com/user-attachments/assets/be05e17a-3ec2-4135-b9c1-a9ff201fa8b5" />



egrep '(World$)' newfile 
## OUTPUT

<img width="539" height="52" alt="image" src="https://github.com/user-attachments/assets/088afb2d-f3ae-41e2-b4da-f963deb3a7b0" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="538" height="50" alt="image" src="https://github.com/user-attachments/assets/71240764-db56-4b89-bc6f-37a6f03231cd" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="538" height="50" alt="image" src="https://github.com/user-attachments/assets/cb078600-160a-45ba-b4eb-201bf3e49fdc" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="538" height="91" alt="image" src="https://github.com/user-attachments/assets/9e01c1d8-345d-44f9-9f23-a241a95c949d" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="538" height="50" alt="image" src="https://github.com/user-attachments/assets/7cdb2156-f6a5-4b71-aaf7-cb22410c86c8" />


egrep l{2} newfile
## OUTPUT

<img width="536" height="72" alt="image" src="https://github.com/user-attachments/assets/1badc944-1e75-427b-8117-15fd407b0348" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="536" height="95" alt="image" src="https://github.com/user-attachments/assets/a1645f1e-3329-474d-b17a-2d3295ebc984" />


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

<img width="450" height="52" alt="image" src="https://github.com/user-attachments/assets/d52bb75b-a8f7-4ee2-abab-2861279184ab" />


sed -n -e '$p' file23
## OUTPUT

<img width="450" height="52" alt="image" src="https://github.com/user-attachments/assets/e9fee75c-a8ad-4d07-a546-10c7df4fce14" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="489" height="204" alt="image" src="https://github.com/user-attachments/assets/e52fa481-4b36-4870-b97f-e0337325d62a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="506" height="205" alt="image" src="https://github.com/user-attachments/assets/2077da9b-7f92-497f-9e84-1eed376e51bf" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="521" height="205" alt="image" src="https://github.com/user-attachments/assets/cb105e00-3139-4a14-8584-b45b0b0ca333" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="483" height="143" alt="image" src="https://github.com/user-attachments/assets/5851bde8-b59e-4b36-9656-c68fca14a7c6" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="495" height="182" alt="image" src="https://github.com/user-attachments/assets/9996baee-2f1b-434a-97e4-8a06459bbc4c" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="541" height="161" alt="image" src="https://github.com/user-attachments/assets/c173096d-b143-4147-bb8d-84ec767f5655" />



seq 10 
## OUTPUT
<img width="541" height="246" alt="image" src="https://github.com/user-attachments/assets/6ffd941c-fe62-4c02-9351-875ad94e683f" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="541" height="99" alt="image" src="https://github.com/user-attachments/assets/883d3a13-b80e-44e4-82ab-5d8921288e78" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="541" height="99" alt="image" src="https://github.com/user-attachments/assets/0b5d7a8e-70e9-4a94-9444-ba9a4bc80453" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="541" height="116" alt="image" src="https://github.com/user-attachments/assets/cb8716b4-cac1-40d1-b43b-9c3e8bce878f" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="480" height="98" alt="image" src="https://github.com/user-attachments/assets/32cf86c1-42b9-4796-863d-26f6bd887185" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="480" height="95" alt="image" src="https://github.com/user-attachments/assets/c36e52cd-6fd1-487f-aff0-369b76b6d31b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="512" height="95" alt="image" src="https://github.com/user-attachments/assets/3f6d3a8e-4367-44cb-9fb7-1808054bd358" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="512" height="95" alt="image" src="https://github.com/user-attachments/assets/ff4b2b08-1358-44a7-8d2c-d3b066c82653" />


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
<img width="350" height="116" alt="image" src="https://github.com/user-attachments/assets/58302bfa-abb7-411b-a736-18bc2421c093" />


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
<img width="350" height="116" alt="image" src="https://github.com/user-attachments/assets/19470e60-f76a-4d75-b044-2d24b5d3157f" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="575" height="208" alt="image" src="https://github.com/user-attachments/assets/c9cfa687-dd18-45f4-ba46-de6a017439f1" />

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
<img width="488" height="95" alt="image" src="https://github.com/user-attachments/assets/8b8a7cf9-8777-4df2-a5a6-c525e494ebe7" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="604" height="95" alt="image" src="https://github.com/user-attachments/assets/ec9879c8-5d2c-4ad0-a4e3-2556c1538eac" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="450" height="205" alt="image" src="https://github.com/user-attachments/assets/e6400714-0ba8-4494-8505-648fdaac6a49" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="591" height="270" alt="image" src="https://github.com/user-attachments/assets/082b01dd-6dd3-45c5-b2d7-0a9514042ccc" />



tar -xvf backup.tar
## OUTPUT
<img width="531" height="201" alt="image" src="https://github.com/user-attachments/assets/95fce389-5695-4a22-9578-327c0b9a9de4" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="398" height="50" alt="image" src="https://github.com/user-attachments/assets/da7a80aa-e37f-4683-a7d0-9bb879dea07b" />
 

gunzip backup.tar.gz
## OUTPUT
<img width="793" height="53" alt="image" src="https://github.com/user-attachments/assets/cdd986c3-4fd4-4da8-bb2a-a3c8b71bc635" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="793" height="53" alt="image" src="https://github.com/user-attachments/assets/c670beab-67c8-43a8-972b-ae1ddf31d33c" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="563" height="95" alt="image" src="https://github.com/user-attachments/assets/1b944b57-c308-4e6a-82a5-38437c16515d" />


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
<img width="743" height="716" alt="image" src="https://github.com/user-attachments/assets/1029d856-06d7-4288-9c6e-6abe883fa77b" />

 
ls file1
## OUTPUT
<img width="381" height="52" alt="image" src="https://github.com/user-attachments/assets/ebbd4dd3-bf57-4fbe-978f-d22298dd8216" />

echo $?
## OUTPUT 
<img width="381" height="52" alt="image" src="https://github.com/user-attachments/assets/3ea6bb7b-4bbb-4076-81f1-a5da1e311c22" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="589" height="51" alt="image" src="https://github.com/user-attachments/assets/74a5ced4-e7d9-4ba8-a145-b1f20b7d8bb6" />


abcd
 
echo $?
 ## OUTPUT
<img width="589" height="51" alt="image" src="https://github.com/user-attachments/assets/ef44c58b-724a-4065-99d4-5952d7e9f8ed" />



 
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
<img width="589" height="225" alt="image" src="https://github.com/user-attachments/assets/aa9c4c49-29fc-41db-96c2-44fecded7cd9" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="613" height="95" alt="image" src="https://github.com/user-attachments/assets/c99a5862-5406-466a-b6c5-aae494721a8d" />


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
<img width="640" height="72" alt="image" src="https://github.com/user-attachments/assets/0bc018a6-6b8c-4056-b3dc-409d7bd7071a" />

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
<img width="640" height="140" alt="image" src="https://github.com/user-attachments/assets/e0103ebc-a67f-4f19-9abd-8bb4ec4f3b09" />



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
<img width="640" height="140" alt="image" src="https://github.com/user-attachments/assets/ff5cebdc-86ed-4b17-9ff0-b8e000200296" />

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
<img width="640" height="135" alt="image" src="https://github.com/user-attachments/assets/b126672b-ae90-47ec-ab32-520683234942" />


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
<img width="640" height="97" alt="image" src="https://github.com/user-attachments/assets/b46b36ca-d22a-4bef-9223-a8ed5197ffd0" />


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
<img width="660" height="73" alt="image" src="https://github.com/user-attachments/assets/4be05f34-8981-48dd-bc6c-161bf03e5ed7" />

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
<img width="502" height="73" alt="image" src="https://github.com/user-attachments/assets/304f0960-d6ca-4f04-895a-65b22ade6a98" />

 
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
<img width="502" height="274" alt="image" src="https://github.com/user-attachments/assets/8e540a3c-4d72-4f8f-b6e1-813929065ac0" />

 
 
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
## Output
<img width="522" height="164" alt="image" src="https://github.com/user-attachments/assets/2556083e-244d-441a-9507-eadd3ce68687" />

 
 
 
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
## OUTPUT
<img width="605" height="229" alt="image" src="https://github.com/user-attachments/assets/49383b92-e999-41c7-b547-8c31dd4ba1a7" />

 
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
## OUTPUT
<img width="605" height="165" alt="image" src="https://github.com/user-attachments/assets/7ed7725d-b122-4f24-911b-4445130b7406" />

 
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
## OUTPUT
<img width="605" height="228" alt="image" src="https://github.com/user-attachments/assets/5ac83e33-e160-430f-84d9-bccae7585f14" />

 
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
<img width="605" height="229" alt="image" src="https://github.com/user-attachments/assets/0b02fb50-f86c-45ff-9bd7-4321cf3db17d" />

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
## OUTPUT
<img width="697" height="76" alt="image" src="https://github.com/user-attachments/assets/8b148ea7-da67-4e7b-bb39-0307478b07e6" />

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="697" height="76" alt="image" src="https://github.com/user-attachments/assets/75509d5c-bbcf-477b-81ae-cd45c6542512" />


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
<img width="385" height="141" alt="image" src="https://github.com/user-attachments/assets/a2c0fe28-4a84-4c99-87ef-843a875113d5" />

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
<img width="504" height="163" alt="image" src="https://github.com/user-attachments/assets/37a861c3-0aed-47a9-8bf5-ed4edec54aae" />

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
<img width="504" height="319" alt="image" src="https://github.com/user-attachments/assets/0086c712-f505-4643-b7c0-903e74e76a31" />

 
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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
<img width="711" height="99" alt="image" src="https://github.com/user-attachments/assets/8553f7c7-f2e4-4948-b89a-0783f5bdbc0d" />
 
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
 <img width="734" height="166" alt="image" src="https://github.com/user-attachments/assets/dfa0efd6-a88b-406f-9b47-0ab1d265fb2e" />

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
<img width="734" height="97" alt="image" src="https://github.com/user-attachments/assets/198762db-4a3d-479b-90c7-5c37a471813a" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="734" height="97" alt="image" src="https://github.com/user-attachments/assets/f2cfd642-ce00-4cb5-91b8-c286b8741f14" />



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
<img width="523" height="77" alt="image" src="https://github.com/user-attachments/assets/40aac67f-c91f-4b0b-b90d-0ff5cd39cb45" />
 
 ./funcex.sh 1 2
<img width="395" height="54" alt="image" src="https://github.com/user-attachments/assets/0031c0ae-43d8-4783-984d-f2ef94d29db4" />

 
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
<img width="485" height="117" alt="image" src="https://github.com/user-attachments/assets/6f3c7377-8395-489d-9f4c-cdcf52e607b4" />

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
 <img width="432" height="95" alt="image" src="https://github.com/user-attachments/assets/b6cb9828-bc7d-4313-8c87-1924afb5bde5" />

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
 <img width="798" height="359" alt="image" src="https://github.com/user-attachments/assets/02a57ea5-ae4a-4832-a56b-614e94e32f67" />

 
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
 <img width="458" height="315" alt="WhatsApp Image 2026-05-10 at 8 19 38 PM" src="https://github.com/user-attachments/assets/9748f4d8-5ede-4ae3-b14a-34d73d85b8e0" />


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

<img width="458" height="99" alt="WhatsApp Image 2026-05-10 at 8 19 40 PM" src="https://github.com/user-attachments/assets/40023663-59a7-4059-b35c-31ffdf4cb194" />


# RESULT:
The Commands are executed successfully.
