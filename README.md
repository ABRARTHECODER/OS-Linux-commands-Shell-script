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

<img width="508" height="400" alt="Screenshot 2026-07-29 091503" src="https://github.com/user-attachments/assets/a77abd40-cdb4-4913-8d88-209af04d902a" />


cat < file2
## OUTPUT

<img width="487" height="417" alt="Screenshot 2026-07-29 091535" src="https://github.com/user-attachments/assets/2853f5ca-3d96-4cb0-81a7-4ec0dde017a8" />


# Comparing Files
cmp file1 file2
 
comm file1 file2

 
diff file1 file2
## OUTPUT
<img width="951" height="702" alt="Screenshot 2026-07-29 092104" src="https://github.com/user-attachments/assets/103fd095-13de-4b30-a2c1-a388502e9301" />


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





cut -d "|" -f 1 file22
## OUTPUT
<img width="468" height="112" alt="Screenshot 2026-07-29 092816" src="https://github.com/user-attachments/assets/3d21bd0c-ceb7-4abe-9911-eb1c8f4c0e38" />
<img width="527" height="121" alt="Screenshot 2026-07-29 092825" src="https://github.com/user-attachments/assets/3cbb077a-11bb-46aa-bc36-9982a4fa523a" />
<img width="463" height="115" alt="Screenshot 2026-07-29 092829" src="https://github.com/user-attachments/assets/116760b0-4822-47b0-8980-7528e407d810" />
<img width="413" height="212" alt="Screenshot 2026-07-29 092837" src="https://github.com/user-attachments/assets/f070d679-52e4-4511-b269-b3597f91ad12" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="390" height="122" alt="image" src="https://github.com/user-attachments/assets/f2732e5a-d7a0-4459-a4f1-078e218ec329" />



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

<img width="287" height="73" alt="Screenshot 2026-07-29 093542" src="https://github.com/user-attachments/assets/64a681de-685f-4613-8bce-492b1069ba29" />


grep hello newfile 
## OUTPUT
<img width="297" height="75" alt="Screenshot 2026-07-29 093549" src="https://github.com/user-attachments/assets/43038623-6a66-41f2-8243-b8fe26b9acd3" />





grep -v hello newfile 
## OUTPUT

<img width="353" height="77" alt="Screenshot 2026-07-29 093553" src="https://github.com/user-attachments/assets/89060ae9-bedd-40cc-b5d7-a0e8cde9b79c" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="390" height="100" alt="Screenshot 2026-07-29 093557" src="https://github.com/user-attachments/assets/9535203e-bff0-4281-b663-2c32945809a4" />





cat newfile | grep -i -c "hello"
## OUTPUT

<img width="440" height="76" alt="Screenshot 2026-07-29 093602" src="https://github.com/user-attachments/assets/129c04eb-ae2a-418e-80be-976e93e5218c" />




grep -R ubuntu /etc
## OUTPUT
<img width="1255" height="173" alt="Screenshot 2026-07-29 093609" src="https://github.com/user-attachments/assets/0288a107-d6e3-49c6-a878-1a0d91beb4c6" />


grep -w -n world newfile   
## OUTPUT

<img width="427" height="106" alt="Screenshot 2026-07-29 093616" src="https://github.com/user-attachments/assets/15624d42-82b2-45a4-a363-776fb9d5c385" />


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
<img width="397" height="310" alt="image" src="https://github.com/user-attachments/assets/b9d1a398-28e1-4e48-9040-bf0a81902509" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="352" height="110" alt="Screenshot 2026-07-29 094446" src="https://github.com/user-attachments/assets/a61525d4-179e-4545-a24c-ea02ccb3efa1" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="393" height="100" alt="Screenshot 2026-07-29 094450" src="https://github.com/user-attachments/assets/3c6df535-98db-4c0e-8ebe-8c782f4a4785" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="338" height="68" alt="Screenshot 2026-07-29 094453" src="https://github.com/user-attachments/assets/4f57c954-82ae-4ee0-826b-9927f9f6b4fe" />



egrep '(world$)' newfile 
## OUTPUT

<img width="367" height="93" alt="Screenshot 2026-07-29 094457" src="https://github.com/user-attachments/assets/82a6caea-ccfc-4099-9b4e-9840bfc904f2" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="357" height="120" alt="Screenshot 2026-07-29 094504" src="https://github.com/user-attachments/assets/8faf7b48-9cbc-4cfd-912d-64b2a5eb0bd5" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="317" height="76" alt="Screenshot 2026-07-29 094516" src="https://github.com/user-attachments/assets/224ebe86-a9be-413a-b6fc-069f02c17ab7" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="350" height="73" alt="Screenshot 2026-07-29 094521" src="https://github.com/user-attachments/assets/a23201cc-bdd1-4c16-95d5-f2f4ee792e88" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="375" height="77" alt="Screenshot 2026-07-29 094637" src="https://github.com/user-attachments/assets/b08c9874-65c0-4cf5-aa71-fd171c4017c8" />

egrep l{2} newfile
## OUTPUT

<img width="277" height="98" alt="Screenshot 2026-07-29 094644" src="https://github.com/user-attachments/assets/13652d18-2bdc-4db5-9f1c-900cc76b64b5" />


egrep 's{1,2}' newfile
## OUTPUT

<img width="332" height="130" alt="Screenshot 2026-07-29 094649" src="https://github.com/user-attachments/assets/03b76704-3803-44d7-bbd8-4fe2f2bc0341" />

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
<img width="943" height="327" alt="Screenshot 2026-07-28 204016" src="https://github.com/user-attachments/assets/c386a073-c7a4-445d-91e5-a7373660318b" />



sed -n -e '$p' file23
## OUTPUT

<img width="930" height="72" alt="Screenshot 2026-07-28 204051" src="https://github.com/user-attachments/assets/1151d737-bf98-4811-91bb-222f270f86c3" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="946" height="277" alt="Screenshot 2026-07-28 204056" src="https://github.com/user-attachments/assets/28247732-9f2d-4bae-ab71-210f5a09cd2f" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="925" height="253" alt="Screenshot 2026-07-28 204121" src="https://github.com/user-attachments/assets/1e5ae557-8e6b-456f-9ee7-396f93e001e7" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="912" height="250" alt="Screenshot 2026-07-28 204126" src="https://github.com/user-attachments/assets/238e66f8-00dc-4f60-85b6-6675c448f3ba" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="945" height="180" alt="Screenshot 2026-07-28 204202" src="https://github.com/user-attachments/assets/4977ac42-a8f1-4ec9-8bf3-a0ac53e7011d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="927" height="130" alt="Screenshot 2026-07-28 204211" src="https://github.com/user-attachments/assets/4ffa7aea-31d4-427f-883d-343bebc652ff" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="941" height="105" alt="Screenshot 2026-07-28 204216" src="https://github.com/user-attachments/assets/1fd48f21-4ffb-41ab-afaf-4159de482e18" />




seq 10 
## OUTPUT
<img width="933" height="305" alt="Screenshot 2026-07-28 204428" src="https://github.com/user-attachments/assets/67af5b2c-1c1d-4f09-baab-5b3f8f39fba4" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="935" height="125" alt="Screenshot 2026-07-28 204456" src="https://github.com/user-attachments/assets/7fa9fa23-d5f1-41ae-9026-828df4c98801" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="893" height="133" alt="Screenshot 2026-07-28 204500" src="https://github.com/user-attachments/assets/5429effd-6ade-4afe-9fa5-cb966fe697c0" />


seq 3 | sed '2a hello'
## OUTPUT
![Uploading Screenshot 2026-07-28 204505.png…]()



seq 2 | sed '2i hello'
## OUTPUT
<img width="923" height="127" alt="Screenshot 2026-07-28 204535" src="https://github.com/user-attachments/assets/7d4ffb0e-5c77-4e91-912b-02a406bf5851" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="938" height="137" alt="Screenshot 2026-07-28 204543" src="https://github.com/user-attachments/assets/de9266c4-890d-4dab-85d9-8c9c18edd3b0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="925" height="125" alt="Screenshot 2026-07-28 204548" src="https://github.com/user-attachments/assets/4f181acc-b02f-476f-baff-2e221b09efb5" />



sed -n '2,4{s/$/*/;p}' file23

<img width="915" height="130" alt="Screenshot 2026-07-28 204614" src="https://github.com/user-attachments/assets/a89445d4-9acd-4219-84c2-610d79801986" />

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
<img width="935" height="358" alt="Screenshot 2026-07-28 204732" src="https://github.com/user-attachments/assets/ac1d1a6c-b5ff-4aff-b6f5-b45fff4b7e3c" />


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

<img width="921" height="376" alt="Screenshot 2026-07-28 204805" src="https://github.com/user-attachments/assets/65dbe156-a8bc-4171-b9e4-bcfb354359d3" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="927" height="255" alt="Screenshot 2026-07-28 204822" src="https://github.com/user-attachments/assets/0b943e07-aaec-416f-8eb6-0fe0a2f75ccc" />

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

<img width="930" height="437" alt="Screenshot 2026-07-28 205039" src="https://github.com/user-attachments/assets/3771a94f-394c-499e-9233-d5bf2e719575" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="943" height="135" alt="Screenshot 2026-07-28 205058" src="https://github.com/user-attachments/assets/228ff658-2424-4682-9cf6-2a19a2d702db" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="921" height="256" alt="Screenshot 2026-07-28 205114" src="https://github.com/user-attachments/assets/da0cc722-b236-48f7-9dd7-5dc1d1e4c219" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="936" height="406" alt="Screenshot 2026-07-28 205230" src="https://github.com/user-attachments/assets/a474a246-655b-42ba-9419-bbef60bad987" />


tar -xvf backup.tar
## OUTPUT
<img width="935" height="255" alt="Screenshot 2026-07-28 205309" src="https://github.com/user-attachments/assets/aa0207df-466d-42bc-be0b-1210c4bc3756" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="930" height="228" alt="Screenshot 2026-07-28 205401" src="https://github.com/user-attachments/assets/53c2291c-2879-41ef-a2ba-137e3c8de13a" />

gunzip backup.tar.gz
## OUTPUT
<img width="920" height="58" alt="Screenshot 2026-07-28 205415" src="https://github.com/user-attachments/assets/680e319a-dd35-4a7f-89e1-401bff195f90" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="935" height="171" alt="Screenshot 2026-07-28 205710" src="https://github.com/user-attachments/assets/40ffe849-cb96-46f6-a608-f5c510046b3b" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="920" height="282" alt="Screenshot 2026-07-28 205759" src="https://github.com/user-attachments/assets/d3f97ed3-5d05-4275-a9c4-a2fb06c6d816" />


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

 <img width="926" height="653" alt="Screenshot 2026-07-28 205911" src="https://github.com/user-attachments/assets/77dcd3c6-aa11-4bc9-b84f-6f677ce73a4c" />
<img width="937" height="480" alt="Screenshot 2026-07-28 210040" src="https://github.com/user-attachments/assets/8790e324-d274-4cd9-a1dd-4ffea94f0e97" />

ls file1
## OUTPUT
<img width="938" height="77" alt="Screenshot 2026-07-28 210103" src="https://github.com/user-attachments/assets/95b1293c-87ba-43a0-b14e-9cba5ce1378d" />

echo $?
## OUTPUT 
<img width="930" height="71" alt="Screenshot 2026-07-28 210109" src="https://github.com/user-attachments/assets/cb1b1dbb-3fb8-49ab-be9c-322b11d1baf4" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="921" height="152" alt="Screenshot 2026-07-28 210143" src="https://github.com/user-attachments/assets/b100fe72-b480-4cc5-9310-800d1c7c9b2b" />

abcd
 
echo $?
 ## OUTPUT
<img width="930" height="162" alt="Screenshot 2026-07-28 210213" src="https://github.com/user-attachments/assets/a6ff5d42-7b84-4ba4-bb2c-c47b668a6ed7" />


 
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
<img width="940" height="586" alt="Screenshot 2026-07-28 210307" src="https://github.com/user-attachments/assets/34b10876-e312-44e0-8cf3-5bb099e2ec2b" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="925" height="158" alt="Screenshot 2026-07-28 210331" src="https://github.com/user-attachments/assets/21a1ccbb-1594-4f0e-8b50-353b30fd89e5" />


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
<img width="910" height="825" alt="Screenshot 2026-07-28 210602" src="https://github.com/user-attachments/assets/6c2e6b15-95e6-4ebc-8163-ddd972e0fda9" />

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
<img width="941" height="596" alt="Screenshot 2026-07-28 210822" src="https://github.com/user-attachments/assets/0c5b55dd-fbf4-4d1b-8441-aa68dbe0e26a" />
<img width="926" height="482" alt="Screenshot 2026-07-28 210742" src="https://github.com/user-attachments/assets/2fdf9114-37b1-4542-b9cc-83fd79ec6f50" />



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
<img width="940" height="781" alt="Screenshot 2026-07-28 210922" src="https://github.com/user-attachments/assets/04c45d58-3289-472e-8d90-617be64431d4" />

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
<img width="946" height="497" alt="Screenshot 2026-07-28 211050" src="https://github.com/user-attachments/assets/2e6d6c4f-57d4-4162-9aa8-83938462028e" />
<img width="930" height="490" alt="Screenshot 2026-07-28 211056" src="https://github.com/user-attachments/assets/0e55cfb3-78a2-4d3e-9415-3528a3fe8c12" />

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
<img width="941" height="497" alt="Screenshot 2026-07-28 211324" src="https://github.com/user-attachments/assets/3cdfa524-4745-4c63-9974-1172d3797144" />
<img width="935" height="492" alt="Screenshot 2026-07-28 211318" src="https://github.com/user-attachments/assets/42504f34-3f20-4681-9ff3-6f5637393587" />


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
<img width="927" height="297" alt="Screenshot 2026-07-28 211514" src="https://github.com/user-attachments/assets/dd89e7ed-24f6-4dd8-901a-a3fa0f0373fe" />

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
 
 <img width="908" height="250" alt="Screenshot 2026-07-28 211710" src="https://github.com/user-attachments/assets/d9612c44-436a-42cf-bf95-e510205b39e9" />

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
 
 <img width="932" height="232" alt="Screenshot 2026-07-28 211803" src="https://github.com/user-attachments/assets/2d86c0a3-c860-41d2-94f2-90dd54a1552f" />

 
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
 <img width="941" height="277" alt="Screenshot 2026-07-28 211918" src="https://github.com/user-attachments/assets/f73400ea-28ea-4c5e-bc77-96a294586780" />

 
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
 
 <img width="940" height="202" alt="Screenshot 2026-07-28 232803" src="https://github.com/user-attachments/assets/ae0336ee-8d4d-42dd-9805-b6fac7bb10ff" />

 
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
 <img width="930" height="302" alt="Screenshot 2026-07-28 232839" src="https://github.com/user-attachments/assets/c34b7ff4-d6d1-45b7-8d2d-4e5c09487e77" />


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

<img width="952" height="641" alt="Screenshot 2026-07-28 232931" src="https://github.com/user-attachments/assets/9497f7d9-571c-44e1-947a-6b680ea1d0d4" />

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
<img width="935" height="557" alt="Screenshot 2026-07-28 233008" src="https://github.com/user-attachments/assets/4a1e7332-6ce3-4892-b7d2-a18a6ca355d9" />

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
<img width="933" height="326" alt="Screenshot 2026-07-28 233425" src="https://github.com/user-attachments/assets/974f4e43-2ab1-4dbd-bb80-ec532ad2ce18" />

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

 <img width="932" height="708" alt="Screenshot 2026-07-28 233509" src="https://github.com/user-attachments/assets/9ad2075d-04c1-4c1b-8d01-a84c99fbbabd" />

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
 <img width="940" height="506" alt="Screenshot 2026-07-28 233554" src="https://github.com/user-attachments/assets/62aca787-cad8-4d0c-bca1-285ac0e03b14" />

cat forcontinue.sh 
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
 <img width="895" height="587" alt="Screenshot 2026-07-28 233712" src="https://github.com/user-attachments/assets/ef9b463e-dc8d-447e-8532-5159d5183c82" />

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
<img width="925" height="325" alt="Screenshot 2026-07-28 233804" src="https://github.com/user-attachments/assets/c5be0741-4448-4342-852b-63d9293cbc01" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



<img width="930" height="305" alt="Screenshot 2026-07-28 233855" src="https://github.com/user-attachments/assets/110daea2-e941-49de-ad18-becd6dc2bfdb" />

 
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
<img width="931" height="435" alt="Screenshot 2026-07-28 233937" src="https://github.com/user-attachments/assets/3f7bbbf7-f98d-46ec-8f2f-685bb1a70b73" />

 
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
 <img width="930" height="345" alt="Screenshot 2026-07-28 234029" src="https://github.com/user-attachments/assets/eae6fab8-44e3-416b-84c4-a37b44bc2537" />
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
 <img width="941" height="480" alt="Screenshot 2026-07-28 234111" src="https://github.com/user-attachments/assets/c7026c52-8539-4401-90b7-d3b3228c9cb9" />

cat argshift2.sh
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
 ./argshift2.sh 1 2 3
 <img width="925" height="351" alt="Screenshot 2026-07-28 234516" src="https://github.com/user-attachments/assets/c0dd1274-9aae-41c4-9d39-0333ec0f9980" />

 
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
<img width="468" height="320" alt="Screenshot 2026-07-28 234746" src="https://github.com/user-attachments/assets/ea5dd4f1-6a1b-4e33-962e-7792388ace90" />

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
<img width="520" height="300" alt="Screenshot 2026-07-28 234750" src="https://github.com/user-attachments/assets/9022c2f4-c827-425b-8c6c-ad8bfd1d09f4" />

awk -f nc.awk data.dat
## OUTPUT 
<img width="512" height="372" alt="Screenshot 2026-07-28 234758" src="https://github.com/user-attachments/assets/d90d053f-450b-4191-8897-badb9a0e63e3" />

 
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
<img width="878" height="662" alt="Screenshot 2026-07-28 234640" src="https://github.com/user-attachments/assets/61ead210-7dd8-45f6-88a8-be2aad3a991c" />


# RESULT:
The Commands are executed successfully.
