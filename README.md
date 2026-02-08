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
<img width="341" height="102" alt="image" src="https://github.com/user-attachments/assets/0dbcb619-dd43-4841-bed2-ec90016e72b4" />



cat < file2
## OUTPUT
<img width="328" height="162" alt="image" src="https://github.com/user-attachments/assets/bb765009-eda0-4bb2-8d66-d6633743e078" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="362" height="44" alt="image" src="https://github.com/user-attachments/assets/8f218ff6-bc3b-46d9-8496-7bb9ccd89b06" />

comm file1 file2
 ## OUTPUT
<img width="375" height="198" alt="image" src="https://github.com/user-attachments/assets/fe328a3d-873b-46b6-8aa6-16cb8195cb3b" />

 
diff file1 file2
## OUTPUT
<img width="428" height="305" alt="image" src="https://github.com/user-attachments/assets/5d9f7bd4-987e-48b1-897e-53f119da7c39" />


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

<img width="383" height="84" alt="image" src="https://github.com/user-attachments/assets/b6ca6183-ca84-41f8-a5e1-72030885c5b1" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="433" height="109" alt="image" src="https://github.com/user-attachments/assets/0ed38233-8971-4fa5-90a7-1a3b1d369acd" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="110" alt="image" src="https://github.com/user-attachments/assets/c3e41e7d-de94-4dcb-b5cb-8edba18c78f1" />


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
<img width="409" height="56" alt="image" src="https://github.com/user-attachments/assets/252efd85-f3cc-4899-b7ee-50f993798c1f" />



grep hello newfile 
## OUTPUT
<img width="400" height="58" alt="image" src="https://github.com/user-attachments/assets/47de37e7-9df9-418a-bbfb-d8ab12b671af" />




grep -v hello newfile 
## OUTPUT
<img width="430" height="59" alt="image" src="https://github.com/user-attachments/assets/7938d054-f2e3-4bba-8f00-e0f6532e5439" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="546" height="81" alt="image" src="https://github.com/user-attachments/assets/29b93fb9-4e18-47f8-926f-03e8481a8230" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="578" height="52" alt="image" src="https://github.com/user-attachments/assets/2be27725-4bbf-46dc-9473-563a2e295e49" />




grep -R ubuntu /etc
## OUTPUT
<img width="609" height="218" alt="image" src="https://github.com/user-attachments/assets/1dd2560b-fbe9-4942-bed7-17811c5453d1" />



grep -w -n world newfile   
## OUTPUT
<img width="474" height="80" alt="image" src="https://github.com/user-attachments/assets/9b9098c0-9bf2-4bdd-bc8e-10a07fb90405" />


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
<img width="563" height="78" alt="image" src="https://github.com/user-attachments/assets/359d55a4-b535-483b-bd6d-47452d93fea1" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/937ba4b2-5988-4f46-83bd-280557849bb6" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/1ab5287e-be27-4d2b-9ba6-7f45bf336a64" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="489" height="58" alt="image" src="https://github.com/user-attachments/assets/e78a6172-a3de-4429-8e72-e34b4d7eacae" />



egrep '(world$)' newfile 
## OUTPUT

<img width="495" height="54" alt="image" src="https://github.com/user-attachments/assets/71ea6252-d06c-489a-b6be-dd103168cba8" />


egrep '(World$)' newfile 
## OUTPUT
<img width="485" height="49" alt="image" src="https://github.com/user-attachments/assets/7192f144-ba70-4ef7-80e3-69d1cd0643e1" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="559" height="76" alt="image" src="https://github.com/user-attachments/assets/c350a8a6-f2ac-4088-9140-6c56a530db1e" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="475" height="62" alt="image" src="https://github.com/user-attachments/assets/0a6cfce3-1145-4324-a012-e9f73b75d371" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="547" height="55" alt="image" src="https://github.com/user-attachments/assets/ea4c5fed-5933-4c2e-a899-0cd874aa0a6f" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="540" height="57" alt="image" src="https://github.com/user-attachments/assets/72748e5c-86b9-4105-88fc-452dc26bdb83" />


egrep l{2} newfile
## OUTPUT
<img width="549" height="76" alt="image" src="https://github.com/user-attachments/assets/645d2137-cdfd-4175-bdc1-c65ea3d9374d" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="492" height="116" alt="image" src="https://github.com/user-attachments/assets/c2cbb080-f4a0-4857-9208-e3b4a5258556" />


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
<img width="446" height="52" alt="image" src="https://github.com/user-attachments/assets/26ef3e32-ae83-4d77-b0ab-bedd76bd06e3" />



sed -n -e '$p' file23
## OUTPUT
<img width="463" height="58" alt="image" src="https://github.com/user-attachments/assets/5fa6280c-083e-4c9a-beb0-1029671f4535" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="520" height="243" alt="image" src="https://github.com/user-attachments/assets/b9312515-c393-40f9-a8f8-d06bc66a73e5" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="521" height="237" alt="image" src="https://github.com/user-attachments/assets/924d78a2-6ff0-4143-b13c-5ab70c2028ca" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="555" height="245" alt="image" src="https://github.com/user-attachments/assets/4fd9ec9f-69b9-4640-a890-4f62ca09a2ca" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="481" height="169" alt="image" src="https://github.com/user-attachments/assets/b5bbf561-5af6-4bec-a8d6-581947373088" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="520" height="108" alt="image" src="https://github.com/user-attachments/assets/12e67cef-7529-4a04-b2b9-e9ccb38c6b36" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="560" height="83" alt="image" src="https://github.com/user-attachments/assets/359a6ed8-9706-422e-b439-05f4b609ff41" />



seq 10 
## OUTPUT
<img width="470" height="241" alt="image" src="https://github.com/user-attachments/assets/6e2b785d-e910-4e04-b44a-4a028ed88e2a" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/7f15a008-0a21-4569-ac30-4b7f7b40c0ff" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/8eee58a9-fdd9-4bf2-b575-c2eac6dd4472" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="476" height="116" alt="image" src="https://github.com/user-attachments/assets/ffd87372-c552-45c6-b96e-11022988f0b2" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/097f3277-d23a-42fb-bff6-aba27afa0bbe" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/693b322b-65ba-4342-9af9-b50b5e1029b0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="542" height="102" alt="image" src="https://github.com/user-attachments/assets/6d8ddcd2-899d-47cf-9e08-f931218538ff" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="565" height="112" alt="image" src="https://github.com/user-attachments/assets/f78cfd79-6ac5-4182-ad89-ee7625396e8f" />

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
<img width="343" height="156" alt="image" src="https://github.com/user-attachments/assets/b8c2d4b7-2624-4bdf-836d-b280ab298d5a" />


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
<img width="363" height="160" alt="image" src="https://github.com/user-attachments/assets/fc329060-d42b-410b-bdf4-8e4745a6a9ef" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="652" height="243" alt="image" src="https://github.com/user-attachments/assets/bad19a45-d1aa-4624-aa5b-1cc85e286545" />

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
<img width="536" height="113" alt="image" src="https://github.com/user-attachments/assets/1cc5cc00-160f-4132-8861-577703e95934" />


 
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


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="337" height="97" alt="image" src="https://github.com/user-attachments/assets/53497101-bc58-4fc4-86f9-1b46c4f0a5a7" />


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
<img width="430" height="331" alt="image" src="https://github.com/user-attachments/assets/f92f3999-872a-4eab-a1d8-7ba4a476822b" />

 
ls file1
## OUTPUT
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/6b466065-fc0a-41f3-b72a-af1e2463e723" />

echo $?
## OUTPUT 
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/a62cb0df-44c2-4eb6-a585-ee0625848b28" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/3a7085ed-415b-401e-81e7-ddb358d5c666" />

abcd
 
echo $?
 ## OUTPUT
<img width="469" height="221" alt="image" src="https://github.com/user-attachments/assets/3734e3fa-7b53-4a35-b356-486182fcfa80" />


 
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
<img width="476" height="243" alt="image" src="https://github.com/user-attachments/assets/c8988e15-bd7e-4fbc-90b7-b58792152690" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="725" height="222" alt="image" src="https://github.com/user-attachments/assets/b4de53ad-9521-4a80-aacc-449b8db0d14f" />


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
<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/294cf245-9b79-4a70-bd21-1bb47f7d87cb" />

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
<img width="524" height="391" alt="image" src="https://github.com/user-attachments/assets/0e6cd444-f780-4875-8133-c19539a45213" />



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
## OUTPUT
<img width="524" height="391" alt="image" src="https://github.com/user-attachments/assets/dd8674f4-80c0-453b-832d-12b700986578" />

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
## OUTPUT
<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/0730cf1d-91e5-43d9-89da-994dde3198fe" />

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
<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/2e23f89b-a75f-4f9d-a88f-817df6c7d389" />


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
<img width="541" height="248" alt="image" src="https://github.com/user-attachments/assets/8177e846-e99f-4855-8d14-50ce097bd4e1" />

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
<img width="504" height="160" alt="image" src="https://github.com/user-attachments/assets/d61d981b-694f-4dd0-b736-7e8029916c69" />

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
<img width="446" height="201" alt="image" src="https://github.com/user-attachments/assets/8cf1c20a-2b82-4134-9fb4-8d1b20b36e99" />


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
<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/4a90ca87-e14b-4d50-a6b6-1dbed82c79e9" />

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
<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/586040a3-ea19-43d6-a47d-02b8debd24dc" />

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
<img width="412" height="201" alt="image" src="https://github.com/user-attachments/assets/5062367f-2e3f-4f48-b710-75b5823717b5" />

 
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
<img width="756" height="275" alt="image" src="https://github.com/user-attachments/assets/c3730244-90cd-4605-a148-502142bb340a" />

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
<img width="481" height="144" alt="image" src="https://github.com/user-attachments/assets/148ee4fd-9000-4ebe-a273-24d4d6e95d74" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="774" height="137" alt="image" src="https://github.com/user-attachments/assets/e232cdbf-3840-49f1-a397-1a11877909a3" />



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

<img width="755" height="44" alt="image" src="https://github.com/user-attachments/assets/67a62aaa-157f-4e01-a8aa-9b97472ad2a0" />

 
./funcex.sh 1 2

<img width="762" height="38" alt="image" src="https://github.com/user-attachments/assets/3e33b5d0-2080-4e5e-971c-6d549a7c9178" />

 
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
<img width="758" height="63" alt="image" src="https://github.com/user-attachments/assets/36a18ae9-35e0-47b5-b28e-d84c927cbeab" />

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
<img width="762" height="87" alt="image" src="https://github.com/user-attachments/assets/1350d147-3ec4-4ef5-add1-3d30100cdbaa" />

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
 <img width="765" height="327" alt="image" src="https://github.com/user-attachments/assets/f9f707f6-5930-4513-8292-068bbc0964b7" />

 
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
<img width="783" height="218" alt="image" src="https://github.com/user-attachments/assets/b0fcf24f-9be4-4d43-9f11-06cb5fb51ea7" />

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
<img width="772" height="70" alt="image" src="https://github.com/user-attachments/assets/adb5393c-330b-4aba-a359-c3f5e037aa68" />


# RESULT:
The Commands are executed successfully.
