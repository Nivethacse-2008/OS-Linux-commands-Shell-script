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

<img width="456" height="154" alt="Screenshot 2026-04-30 133128" src="https://github.com/user-attachments/assets/12848d93-84ef-4c41-b8f8-8c367d910cea" />


cat < file2
## OUTPUT

<img width="411" height="202" alt="Screenshot 2026-04-30 133137" src="https://github.com/user-attachments/assets/989f0b7e-3b5f-4c1e-959b-0ecaa6eaebd7" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="377" height="128" alt="Screenshot 2026-04-30 133146" src="https://github.com/user-attachments/assets/92b3e954-d0d1-4956-884f-f973cdb5333e" />

 
comm file1 file2
 ## OUTPUT

<img width="486" height="229" alt="Screenshot 2026-04-30 133315" src="https://github.com/user-attachments/assets/a2ad6141-2b83-4b71-9de9-a49f71b1f0bf" />

 
diff file1 file2
## OUTPUT

<img width="418" height="278" alt="Screenshot 2026-04-30 133323" src="https://github.com/user-attachments/assets/63b2bfb8-6d6d-48af-86fe-08df0abfec25" />



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


<img width="335" height="149" alt="Screenshot 2026-05-01 184010" src="https://github.com/user-attachments/assets/772a218e-d190-46d4-9d7e-d912bc448048" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="363" height="153" alt="Screenshot 2026-05-01 184044" src="https://github.com/user-attachments/assets/1fbb72b6-e771-49cd-a2e3-1d646f89bcf5" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="427" height="398" alt="Screenshot 2026-05-01 104348" src="https://github.com/user-attachments/assets/3c875226-a90a-4f4c-950e-a9acbd68d93a" />


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

<img width="296" height="77" alt="Screenshot 2026-05-01 104604" src="https://github.com/user-attachments/assets/734af28e-b768-4de8-a62d-e0c19ce83958" />


grep hello newfile 
## OUTPUT

<img width="354" height="75" alt="Screenshot 2026-05-01 104629" src="https://github.com/user-attachments/assets/9dd209c5-9b06-466b-8ee3-f24b6420e136" />



grep -v hello newfile 
## OUTPUT

<img width="399" height="99" alt="Screenshot 2026-05-01 104658" src="https://github.com/user-attachments/assets/37669a48-1a0a-425f-8b01-336cb92d1a7b" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="399" height="78" alt="Screenshot 2026-05-01 104730" src="https://github.com/user-attachments/assets/961f7781-574a-4fae-9aaf-653900327d0a" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="644" height="426" alt="image" src="https://github.com/user-attachments/assets/2b7814c7-e2fb-4eba-ac9c-c28e6327fd51" />


grep -R ubuntu /etc
## OUTPUT

<img width="340" height="99" alt="Screenshot 2026-05-01 104751" src="https://github.com/user-attachments/assets/32822591-1b00-4ae7-a13e-14bb8144c99a" />


grep -w -n world newfile   
## OUTPUT

<img width="403" height="108" alt="Screenshot 2026-05-01 104823" src="https://github.com/user-attachments/assets/f18eee96-1313-4272-a9d7-28d4ec3e911b" />


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

<img width="403" height="108" alt="Screenshot 2026-05-01 104823" src="https://github.com/user-attachments/assets/051cc2c8-b7e5-42c9-aa51-36a4c306364d" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="446" height="99" alt="Screenshot 2026-05-01 104856" src="https://github.com/user-attachments/assets/e6d7b862-892f-4c21-ab3d-73d748d44b27" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="342" height="78" alt="Screenshot 2026-05-01 104923" src="https://github.com/user-attachments/assets/4acd0e9b-fea8-4f7a-9759-39d505d2023a" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="382" height="121" alt="Screenshot 2026-05-01 114224" src="https://github.com/user-attachments/assets/7eedb704-b8cf-4d9f-8c87-51ef6698eae9" />


egrep '(world$)' newfile 
## OUTPUT

<img width="382" height="121" alt="Screenshot 2026-05-01 114224" src="https://github.com/user-attachments/assets/71097f29-0483-4986-9bc9-9fed37e5c206" />


egrep '(World$)' newfile 
## OUTPUT

<img width="414" height="125" alt="Screenshot 2026-05-01 114304" src="https://github.com/user-attachments/assets/12a37577-1d60-4f31-bf97-05e7dcde496a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="381" height="73" alt="Screenshot 2026-05-01 114341" src="https://github.com/user-attachments/assets/89bcd540-2d7a-47f4-9110-e0dff6100c75" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="467" height="100" alt="Screenshot 2026-05-01 114456" src="https://github.com/user-attachments/assets/acfe246c-682e-478c-8a69-fa48339d1741" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="467" height="100" alt="Screenshot 2026-05-01 114456" src="https://github.com/user-attachments/assets/51bb3bf4-7baa-4c7a-9f4b-4dcf44daed8d" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="302" height="100" alt="Screenshot 2026-05-01 114545" src="https://github.com/user-attachments/assets/9e7e1be7-979f-4c1c-8b93-aca183365e2d" />


egrep l{2} newfile
## OUTPUT

<img width="335" height="127" alt="Screenshot 2026-05-01 114740" src="https://github.com/user-attachments/assets/9fff27fd-34f8-4178-976c-4a99d0b83c91" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="351" height="67" alt="Screenshot 2026-05-01 115052" src="https://github.com/user-attachments/assets/04671d29-b06d-4f68-88af-205a12d7bf0c" />


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

<img width="246" height="41" alt="image" src="https://github.com/user-attachments/assets/f84c4fe2-194d-4011-b1ab-3502c6275410" />


sed -n -e '$p' file23
## OUTPUT

<img width="437" height="249" alt="Screenshot 2026-05-01 115122" src="https://github.com/user-attachments/assets/23a5825e-3ee0-42a2-aa8e-22e308799eb7" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="439" height="249" alt="Screenshot 2026-05-01 115200" src="https://github.com/user-attachments/assets/55149b77-650a-4f5f-af5f-2f5ed8bdd0f0" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="416" height="250" alt="Screenshot 2026-05-01 115245" src="https://github.com/user-attachments/assets/48350e4f-20bf-4179-8ea1-a99819ebf6d4" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="389" height="177" alt="Screenshot 2026-05-01 115312" src="https://github.com/user-attachments/assets/cc21114c-77a8-4d71-8561-bdec7cf5880b" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="396" height="127" alt="Screenshot 2026-05-01 115350" src="https://github.com/user-attachments/assets/6f45f473-8ece-4387-b800-7e00946e8951" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="396" height="127" alt="Screenshot 2026-05-01 115350" src="https://github.com/user-attachments/assets/001ea3b6-0b2d-461e-a1dc-117cff0da238" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="424" height="100" alt="Screenshot 2026-05-01 115512" src="https://github.com/user-attachments/assets/ef39a9a0-25ff-47af-ad71-9777ae191def" />


seq 10 
## OUTPUT

<img width="261" height="299" alt="Screenshot 2026-05-01 115550" src="https://github.com/user-attachments/assets/370779a7-2bf3-4104-a838-55a2cb5dba9f" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="316" height="126" alt="Screenshot 2026-05-01 115632" src="https://github.com/user-attachments/assets/cea0747a-72f6-4ba8-b4b5-7a0e4cb15e3f" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="329" height="70" alt="image" src="https://github.com/user-attachments/assets/be23173c-8645-4fed-847c-c468ef9def72" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="354" height="150" alt="Screenshot 2026-05-01 115754" src="https://github.com/user-attachments/assets/dc893331-903f-4de5-a86b-d8d5a37f1dd3" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="345" height="123" alt="Screenshot 2026-05-01 115824" src="https://github.com/user-attachments/assets/e9e6d6f3-3aa4-4403-be4d-13a9466ecf1b" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="377" height="126" alt="Screenshot 2026-05-01 115854" src="https://github.com/user-attachments/assets/e43efa8a-7e93-4c84-b891-74924963bd9e" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="405" height="132" alt="Screenshot 2026-05-01 115948" src="https://github.com/user-attachments/assets/5b85ec26-fc5b-4f96-bde5-1621faf36d95" />


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

<img width="353" height="231" alt="Screenshot 2026-05-01 120233" src="https://github.com/user-attachments/assets/f53c0e41-5761-41d9-8d1a-8685edb6ce15" />


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

<img width="369" height="172" alt="Screenshot 2026-05-01 120304" src="https://github.com/user-attachments/assets/b73f5c89-e15a-44ec-8004-a3faf63f98f3" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="374" height="166" alt="image" src="https://github.com/user-attachments/assets/684742c2-0275-418b-a7da-2c9f229754a5" />


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

<img width="314" height="128" alt="Screenshot 2026-05-01 120705" src="https://github.com/user-attachments/assets/8891cf05-5c7f-44cc-b094-d51bd33502ee" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="473" height="130" alt="Screenshot 2026-05-01 120817" src="https://github.com/user-attachments/assets/711d5de0-198a-47fa-a460-0d028d4ceab1" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="357" height="217" alt="image" src="https://github.com/user-attachments/assets/280202c9-72c2-4325-bd82-fed79f39fff7" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="658" height="483" alt="image" src="https://github.com/user-attachments/assets/fd61cbf9-fa84-46b1-8600-81592cc26654" />


tar -xvf backup.tar
## OUTPUT

<img width="420" height="206" alt="image" src="https://github.com/user-attachments/assets/1f0d25b7-eeed-43b9-945b-bb65376aed57" />


gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

<img width="245" height="19" alt="image" src="https://github.com/user-attachments/assets/aa991e6b-424c-4fe0-873c-8211a8671a15" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="539" height="122" alt="image" src="https://github.com/user-attachments/assets/f251b8d8-167e-4515-bc56-91866a3dee01" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="374" height="121" alt="Screenshot 2026-05-01 121952" src="https://github.com/user-attachments/assets/f68bde99-f2f5-4804-b8ef-f550a0ebaf73" />


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

<img width="332" height="41" alt="image" src="https://github.com/user-attachments/assets/1a0a3987-6546-40ba-86ba-15e51fde22f1" />
 
ls file1
## OUTPUT

<img width="269" height="79" alt="Screenshot 2026-05-01 120830" src="https://github.com/user-attachments/assets/1df67b43-fd9c-4eab-9a0c-410152b07f5d" />


echo $?
## OUTPUT 

<img width="338" height="76" alt="Screenshot 2026-05-01 120844" src="https://github.com/user-attachments/assets/614d4567-574b-45de-967c-a84c1e4966cc" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="338" height="76" alt="Screenshot 2026-05-01 120844" src="https://github.com/user-attachments/assets/95479648-de9e-4d39-bea9-93e59a409411" />

abcd
 
echo $?
 ## OUTPUT


 
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

<img width="416" height="271" alt="Screenshot 2026-05-01 122624" src="https://github.com/user-attachments/assets/dc57f635-74f9-4286-9506-83a372cf5272" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="365" height="270" alt="Screenshot 2026-05-01 122807" src="https://github.com/user-attachments/assets/c25d83e7-6975-4379-8de2-72bc71b35516" />


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

<img width="214" height="77" alt="image" src="https://github.com/user-attachments/assets/17839be1-e71e-474c-b88e-e28bb1594ab1" />

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

<img width="214" height="77" alt="Screenshot 2026-05-01 193113" src="https://github.com/user-attachments/assets/c5a0fab6-a8bd-4fb8-a276-5a10bf497859" />


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

<img width="549" height="99" alt="image" src="https://github.com/user-attachments/assets/001c574a-12a2-43fd-936b-65a855297c4a" />

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

<img width="546" height="495" alt="Screenshot 2026-05-01 193940" src="https://github.com/user-attachments/assets/c0242405-94f9-4c57-aa15-374b32770f97" />


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

<img width="620" height="175" alt="image" src="https://github.com/user-attachments/assets/30572d5e-268c-4b21-b285-7045aad13723" />

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

 <img width="363" height="410" alt="Screenshot 2026-05-01 145122" src="https://github.com/user-attachments/assets/35aec0da-6cb6-49d3-9147-b7df42ee796a" />


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

<img width="323" height="144" alt="image" src="https://github.com/user-attachments/assets/7ad9567b-4c14-4355-bb2c-f888afa33d4e" />


# RESULT:
The Commands are executed successfully.
