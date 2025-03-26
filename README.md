# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise

# Linux commands-Shell scripting
Linux commands-Shell scripting
``
### NAME   : Kiruba R C
### REF NO : 212224230125

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
![image](https://github.com/user-attachments/assets/cf018bae-a727-4dcf-b7b6-cc9087db47ff)

cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/2e519014-2a19-4a80-a4fa-01f0a5d2ce85)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/17063e6e-c5da-458b-92a7-13ff9998daeb)


comm file1 file2
 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/ed50161c-c238-45d6-b3e5-e4ba01a14bc6)

diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/3266ba31-6c5f-47b5-ac45-e016441b8e92)


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
![image](https://github.com/user-attachments/assets/1ee4a7df-1571-4944-ac9d-e1c4ee6fb4d2)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/9549faa2-24ee-4e44-8199-f249397dc2ad)



cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/0eaab30a-f5aa-496f-bdf4-108a8aede30d)

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
![image](https://github.com/user-attachments/assets/cf26244a-4ee7-44bd-9afe-26cf1bbb651f)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/90a47ab9-c73e-47f4-9e38-4a2091d56f7d)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b2c7b924-1f12-417a-9d3a-fae3baedbc82)


cat newfile | grep -i "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/d4ef58b7-be4e-4cee-93a3-edba29b3fc08)


cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/1f3b1788-c5ae-4b41-8b98-dcc714f979fb)


grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/677bc9cb-1475-415b-b8bd-b499105007ca)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/ecdebbd5-65cc-4c55-b30b-4c8f0543625e)

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
![image](https://github.com/user-attachments/assets/29532c6b-e697-4a75-ab05-73118cfb8af4)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/eb1e9be5-1c72-4084-8f39-c8801aa987f0)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/9e0daef2-5bdd-47b0-aff9-df6cc8c8d8dd)


egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/5181c1f1-f681-4d25-8ad4-3155c7defe2b)

egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/83c3302e-b39a-48da-ac39-27ad233a0112)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/a702c4f0-1d52-4266-939e-67acffc9c112)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/487ba996-195a-4870-9abb-e0c10ab8e5ac)

egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/70d217f3-2ff1-4614-937c-37dd5d0ca953)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/1532cd8e-3f7a-41f6-a030-3ee04700f4ad)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/30e23b74-6ee0-42d0-8035-7352b713ac2e)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/42c1e5c4-39e1-4b2a-9237-bec00d3e08c9)

egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/7d0c5a8d-d41b-4df7-8eb6-2fbc45926fb3)

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

![image](https://github.com/user-attachments/assets/276980b7-85ac-4ba3-967b-0dcc3d56a9e0)

sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/63c9102f-c3c4-47c6-b05e-e6e79da08a76)

sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/72d10efd-2648-4974-914f-003c24a07402)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/81689dfd-ca45-46b7-99c3-2134be8f0191)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/01f513cc-ce2b-4a3c-9c4b-7ca9708851d1)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/070685c2-f956-4fa5-ae1d-0ebdfd7cb0b0)

sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/d160eba4-e328-4932-aa92-f69a95af4fb9)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/0c92de3a-cd91-4d35-98f2-5ad41b20cd67)

seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/d7754de3-b0af-4b38-8100-77590ff40a03)


seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/caddf198-3c87-440b-9b42-0ff4b9541a53)



seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/a7128079-461a-4a47-9b34-539d0f8f5eab)


seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/215929a8-16d4-4fa0-87b5-88e3b441a26f)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/69249594-aab9-44a9-8f21-a00da9eb8993)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/aa285d39-ae56-43f5-96a2-085cd97d2943)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/767490a2-8088-4c07-8dca-4e651d7cf9ff)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ca091424-b452-4166-8a2f-5047157c4f18)


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

![image](https://github.com/user-attachments/assets/77ee035e-49e6-4989-a029-0f70044d0d3c)

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
![image](https://github.com/user-attachments/assets/f0ecba15-ee0e-431f-a06f-1f0810dbf11d)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/ebbc4de1-0bd4-4f02-b45d-8842a2728439)

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
![image](https://github.com/user-attachments/assets/96fe2014-59ae-4fb2-b2a4-e322c19041f2)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/b630d2c2-442e-4278-aef1-7510c64ac0d0)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/9f70ff0f-990f-4d98-80bc-1af7123c3b95)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/23c51056-688d-4ebb-8434-96bf51225d0c)

tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/8644bfce-ba71-4648-b284-792a4572f091)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/9db43d87-8715-41f1-a433-3bf56a7fb4de)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/bbd8fedb-75d5-43fa-8a01-9fe46b29d362)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/cb2c2280-e47c-445e-9908-5be8914bccbe)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/f2b0b9b0-6e39-4e4c-8910-c9fe422309e9)


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
![image](https://github.com/user-attachments/assets/e5b67867-af9b-4a4e-95d4-b4f8d8e78154)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/3f684f83-55f1-46a5-9ccd-1d24b79425cf)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/461954b2-9d33-4194-8bf7-7643ec418518)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/b04ab3a9-9f41-4e1a-a33b-9221fa636b9f)

abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/e5b8b012-d83b-4f87-899d-e0191204be26)

 
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
![image](https://github.com/user-attachments/assets/7c1e85d6-7604-45f7-b571-a84c53f64e7f)


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
![image](https://github.com/user-attachments/assets/692ca416-ad6a-4f9a-b381-e5cd2c1f86ae)

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
![image](https://github.com/user-attachments/assets/266ab260-5c8c-4788-aafd-ca4d4bbcc5f2)



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
![image](https://github.com/user-attachments/assets/88d8aebb-d32a-4987-8426-a413022efbb7)

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
![image](https://github.com/user-attachments/assets/d510b40b-1461-4b10-ba36-0ad953c1e922)

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
![image](https://github.com/user-attachments/assets/603e8764-d92e-4264-b9a7-0ad9c297ed88)


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
![image](https://github.com/user-attachments/assets/ac9556b9-5b7b-4419-9000-511e33393da2)

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
 ## output
 ![image](https://github.com/user-attachments/assets/5a290371-a1f2-4fb1-b617-2bc60838f53a)

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
 
## output
![image](https://github.com/user-attachments/assets/5cc4d37a-4158-45aa-a03f-44a315a0c4bd)


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
 
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/db18c0c5-9081-4386-a68c-9c355ce51351)

 
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
 $ ./forin2.sh
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/8d237417-b633-4e4a-9ef5-d3352833d603)

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
 $ ./forin3.sh
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/a758bb78-275a-4dbd-af4f-1466f7d065d9)

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
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```




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
![image](https://github.com/user-attachments/assets/a5b30984-08a4-44e8-9208-20105171a0c3)

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
![image](https://github.com/user-attachments/assets/28a50bca-a0f9-48b4-8e32-736a52421e50)

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
![image](https://github.com/user-attachments/assets/f0959f28-d0ea-4596-af33-ce9ee42c98bd)

 
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
![image](https://github.com/user-attachments/assets/2b9ff9eb-c421-43f7-be17-80534ae70235)

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

 
cat exread.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/7e0a5401-2cf3-4890-9a6b-28f68bab86d4)

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
![image](https://github.com/user-attachments/assets/bc316ef4-2b6c-4eac-8cb4-62f1cd22b96e)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 





$ ./exread1.sh 
## OUTPUT
 ![image](https://github.com/user-attachments/assets/0058d1db-7642-4214-b403-2feda95c8ec3)

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
./funcex.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/a64e3dea-a0b2-4ef6-87dc-ce5586af343d)

 

 
 ./funcex.sh 1 2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/ed654d0b-6131-4054-9315-07658e9fbd95)

 
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
![image](https://github.com/user-attachments/assets/496372ba-f016-4811-b096-d4c8346fe431)

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
![image](https://github.com/user-attachments/assets/5a87aa69-a179-43b9-bcd7-ef646c9cefef)

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

 ./argshift.sh 1 2 3
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/948324ae-43c7-49d1-8e2e-bd3f62323c32)

 
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
 ![image](https://github.com/user-attachments/assets/5a974231-3dca-4896-a728-9f7c2df00e26)

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
![image](https://github.com/user-attachments/assets/715391d3-abad-4f7b-905f-e2b063b2bca0)


# RESULT:
The Commands are executed successfully.
