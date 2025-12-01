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


<img width="975" height="210" alt="file1" src="https://github.com/user-attachments/assets/5c7ab96e-1612-4940-9229-b9247e3ded34" />

cat < file2
## OUTPUT

<img width="980" height="243" alt="file2" src="https://github.com/user-attachments/assets/41cbe024-6d6c-4d51-b41b-137e6c1616fd" />

# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT

 <img width="980" height="105" alt="cmp" src="https://github.com/user-attachments/assets/fbcea290-9a56-4d3f-af4f-2b7df7ca2d7b" />

diff file1 file2
## OUTPUT

<img width="975" height="308" alt="comm file1 file2" src="https://github.com/user-attachments/assets/082bf6bd-664a-4ffe-8671-03333dbe72ca" />

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


<img width="970" height="138" alt="cut -c1-3 file11" src="https://github.com/user-attachments/assets/dc024bb5-2570-4b07-8385-05d45192a285" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="975" height="173" alt="cut -d ___ -f 1 file22" src="https://github.com/user-attachments/assets/d9889fdd-a8c7-4445-b632-ab910d67fd69" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="968" height="166" alt="cut -d ___ -f 2 file22" src="https://github.com/user-attachments/assets/b2f167c7-deb3-4d5b-9e83-58b50c0d1ae1" />

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

<img width="982" height="107" alt="grep Hello" src="https://github.com/user-attachments/assets/f38cbc8d-016e-4883-994f-79862ccb127e" />


grep hello newfile 
## OUTPUT


<img width="976" height="105" alt="grep hello" src="https://github.com/user-attachments/assets/44c7a029-6578-4077-97e6-6267f97fc81f" />


grep -v hello newfile 
## OUTPUT

<img width="976" height="105" alt="grep hello" src="https://github.com/user-attachments/assets/e9c95fd3-c386-4f98-bdfc-c58a2e4f697d" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="976" height="105" alt="grep hello" src="https://github.com/user-attachments/assets/f29a6920-c712-467f-acb7-f71c5671d0e1" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="968" height="101" alt="grep -v hello newfile" src="https://github.com/user-attachments/assets/eaaeed4c-e5ad-4b2b-85da-35f189fcb8e8" />



grep -R ubuntu /etc
## OUTPUT

<img width="976" height="136" alt="cat newfile _ grep -i _hello_" src="https://github.com/user-attachments/assets/7809104b-bd35-4a45-b25b-e1b2ef92854d" />


grep -w -n world newfile   
## OUTPUT

<img width="976" height="136" alt="cat newfile _ grep -i _hello_" src="https://github.com/user-attachments/assets/9b503e1b-6dab-4018-aff3-f7664db12229" />

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

<img width="977" height="108" alt="cat newfile _ grep -i -c _hello_" src="https://github.com/user-attachments/assets/d038553e-684a-4e00-b8e3-d6ed86ddfa97" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="1887" height="778" alt="grep -R ubuntu" src="https://github.com/user-attachments/assets/18dce7bd-9360-4e2b-8113-2950be9e5441" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="1030" height="140" alt="grep -w -n world newfile" src="https://github.com/user-attachments/assets/7e3b864d-9f57-4cdf-9f7d-b173b0520e7c" />


egrep '(^hello)' newfile 
## OUTPUT



egrep '(world$)' newfile 
## OUTPUT

<img width="977" height="139" alt="egrep -w &#39;Hello_hello&#39; newfile" src="https://github.com/user-attachments/assets/17658235-f78f-4d1d-95bc-38563aa3dfe1" />


egrep '(World$)' newfile 
## OUTPUT
<img width="977" height="138" alt="egrep -w &#39;(H_h)ello&#39; newfile" src="https://github.com/user-attachments/assets/c96f5604-7080-4728-ab6c-346652d88fa7" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="970" height="137" alt="egrep -w &#39;(H_h)ell a-z &#39; newfile " src="https://github.com/user-attachments/assets/d4bde15c-db62-4071-8836-9531dcf94181" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="973" height="103" alt="egrep &#39;(^hello)&#39; newfile " src="https://github.com/user-attachments/assets/cdc56c73-60fe-48f2-b422-2c00a6888a28" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="973" height="138" alt="egrep &#39;(world$)&#39; newfile" src="https://github.com/user-attachments/assets/50c21e39-45cd-47bb-a5ea-7b11908d29a0" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="973" height="138" alt="egrep &#39;(world$)&#39; newfile" src="https://github.com/user-attachments/assets/83edfe6c-b5e5-45ed-b3f8-37e8012ea1b5" />

egrep l{2} newfile
## OUTPUT


<img width="968" height="99" alt="egrep &#39;(World$)&#39; newfile" src="https://github.com/user-attachments/assets/6a6325e5-aa22-47b8-84a5-2bb6266cda28" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="968" height="99" alt="egrep &#39;(World$)&#39; newfile" src="https://github.com/user-attachments/assets/fe4c9f32-f239-4d2b-9d52-1e70ebcdbe42" />


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

<img width="977" height="170" alt="egrep &#39;((W_w)orld$)&#39; newfile" src="https://github.com/user-attachments/assets/fd595c41-fa03-409e-a27f-2d3d8afdfd39" />


sed -n -e '$p' file23
## OUTPUT

<img width="982" height="99" alt="sed -n -e &#39;$p&#39; file23" src="https://github.com/user-attachments/assets/eba841da-2bf7-4f9d-9b12-f30b35980984" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="970" height="339" alt="sed  -e &#39;sRam" src="https://github.com/user-attachments/assets/ae028542-046d-4d69-a28f-f5babe0fb9c4" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="975" height="335" alt="sed  -e &#39;2s" src="https://github.com/user-attachments/assets/edbbeaff-5b1f-4270-a816-1070f20b618d" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="975" height="335" alt="sed  -e &#39;2s" src="https://github.com/user-attachments/assets/ffed19ed-0d35-4ece-973d-22542c498ff2" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="970" height="345" alt="sed  &#39;pathpath" src="https://github.com/user-attachments/assets/8c497c3d-8eb2-4882-88ad-920ad6dbf80a" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="970" height="345" alt="sed  &#39;pathpath" src="https://github.com/user-attachments/assets/b54cfdeb-db57-4c29-b82e-182f4d4e3086" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="977" height="247" alt="sed -n -e &#39;1,5p&#39; file23" src="https://github.com/user-attachments/assets/86383103-be93-4aaf-a9f8-967123373165" />


seq 10 
## OUTPUT

<img width="982" height="170" alt="sed -n -e &#39;2,Joe" src="https://github.com/user-attachments/assets/0eb312fa-ba04-492a-947b-f6ae8c98eeeb" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="976" height="135" alt="sed -n -e &#39;tom" src="https://github.com/user-attachments/assets/706f902c-69a2-4b6a-9de2-a41511469fa0" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="980" height="410" alt="seq 10 " src="https://github.com/user-attachments/assets/68a3ea75-a7ac-4472-ad1a-e419d85d2d56" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="971" height="172" alt="seq 10 _ sed -n &#39;4,6p&#39;" src="https://github.com/user-attachments/assets/deacd6b5-58b3-4613-b14a-1c0281dc058a" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="977" height="173" alt="seq 10 _ sed -n &#39;2,~4p&#39;" src="https://github.com/user-attachments/assets/3db46b64-e6d4-4401-8bd8-14f7e3b3f9dd" />

seq 10 | sed '2,9c hello'
## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="991" height="202" alt="seq 3 _ sed &#39;2a hello&#39;" src="https://github.com/user-attachments/assets/c8f8d5bf-237c-425f-927d-8efe2eac65ce" />



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
<img width="986" height="172" alt="sed -n &#39;2,4{}&#39; file23" src="https://github.com/user-attachments/assets/57f4ac17-291b-40a3-9510-b1ad833b0113" />


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

<img width="980" height="169" alt="sed -n &#39;2,4{x}&#39; file23" src="https://github.com/user-attachments/assets/f31d0ba1-98cf-4118-91d4-0e1c94c7af4c" />


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

<img width="972" height="238" alt="sort file21" src="https://github.com/user-attachments/assets/6a18910b-5849-4124-a45e-0d2649a0548b" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="971" height="239" alt="uniq file22" src="https://github.com/user-attachments/assets/9933953c-80ad-4851-978a-fa4752c6a60f" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="978" height="341" alt="cat file23 _ tr  _lower_   _upper_" src="https://github.com/user-attachments/assets/2003e33a-02b3-470d-821d-b49b909187b0" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="983" height="179" alt="cat urllist txt _ tr -d &#39; &#39;" src="https://github.com/user-attachments/assets/b4808faf-4d7c-4e74-ab4c-8c66ed4107f2" />


tar -xvf backup.tar
## OUTPUT

gzip backup.tar
<img width="983" height="179" alt="cat urllist txt _ tr -d &#39; &#39;" src="https://github.com/user-attachments/assets/45f8e817-1145-4d7b-9faf-75e0cc70e583" />

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 <img width="973" height="339" alt="tar -cvf backup tar _" src="https://github.com/user-attachments/assets/65174548-e59d-4580-ba78-6d1e30e60e9e" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="973" height="339" alt="tar -cvf backup tar _" src="https://github.com/user-attachments/assets/81ff8781-8178-4243-8dfe-5f5d86cd39e6" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1112" height="341" alt="tar -tvf backup tar" src="https://github.com/user-attachments/assets/3d75e35a-42e5-400b-921e-05524e38e27d" />


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
<img width="1115" height="95" alt="ls _ gz" src="https://github.com/user-attachments/assets/3ee44059-61ef-4d38-a1a6-c1156e20cc85" />

 
ls file1
## OUTPUT
<img width="973" height="138" alt="my-script sh" src="https://github.com/user-attachments/assets/2816605c-4541-4153-a11c-0aed89ba7fd1" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="973" height="138" alt="my-script sh" src="https://github.com/user-attachments/assets/164a458d-509b-460e-8b3f-10f844c43d4c" />

echo $?
## OUTPUT 
 <img width="970" height="205" alt="cat herecheck txt" src="https://github.com/user-attachments/assets/208ca635-8355-45a2-8c7b-f2f9cefd3ba1" />

abcd
 
echo $?
 ## OUTPUT

<img width="970" height="205" alt="cat herecheck txt" src="https://github.com/user-attachments/assets/3e6ecd44-e8ff-4b72-a7a5-d5503c560ae8" />

 
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

<img width="988" height="339" alt="palindrome" src="https://github.com/user-attachments/assets/847e2e1c-f853-4020-af31-bf803fb9f11f" />

# RESULT:
The Commands are executed successfully.
