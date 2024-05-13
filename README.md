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

![O1](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/09cc1f44-6d7a-498e-b172-ffe72186e249)


cat < file2
## OUTPUT
![O2](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/80870417-9bb6-447c-bd2f-c686d87452a2)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![O3](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/f4ffeb85-c8b4-40ed-adbb-8e4c6cc65ae9)

comm file1 file2
 ## OUTPUT
![O4](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/bbc0ec17-619e-467e-a00a-99e5e9dd8b01)

 
diff file1 file2
## OUTPUT
![O5](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/11ea202c-3b46-423e-b3fd-590c9d970787)


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
![O6](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/183836cf-97f0-427a-b74b-ba81733581c2)




cut -d "|" -f 1 file22
## OUTPUT
![O7](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/2c83ca62-c781-4b99-ba29-aa3a0193a833)



cut -d "|" -f 2 file22
## OUTPUT
![O8](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/fdbba56f-636b-4076-adbc-853311a2c50b)


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

![O9](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/b4c5e0ed-c6f4-434d-846b-fbeb7d900cbb)


grep hello newfile 
## OUTPUT
![O10](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/6467322d-7d2f-4b9d-928c-7e90bde6de5f)




grep -v hello newfile 
## OUTPUT
![O11](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/d34c6bc0-240b-4b04-ae1f-55bf237c9359)




cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/6dafb439-2cec-488d-9e7b-5311852487df)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/3d3f5078-9e2b-47c2-bf5c-dbfd65150948)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/b7785818-b86d-4c2b-8968-7ff061f8f83f)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/523dfc66-9a9e-4301-82ca-f2797fe8945d)



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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/a65a9cf1-c177-49e8-a3aa-e9c4e756640a)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/666d174a-375d-4357-b583-5d638cd1c46a)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/abe6e21a-b7d7-49d0-ab87-3bdaeb7b2fb5)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/518f944c-85ec-4bb1-a0ee-577a0016e62c)




egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/d5927e87-b71a-48a0-92c1-0586f228557c)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/8edc719d-3d8e-42f6-bdc0-8028b4a8dffb)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/09d0d5b0-a04e-4464-bb23-4809af5d5109)




egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/d29bb2a3-5726-4629-b3c4-9d5adc73e160)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/fb2c0df1-6dc4-4fd4-b3e5-2292f7847ff9)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/ace1f735-6048-4f7d-bd91-21846380a84c)



egrep l{2} newfile
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/ce734b58-1410-4017-a59d-0533e138ef10)




egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/734f9644-412d-49f7-b6bf-e28bf71b445c)



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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/6b73aac1-a654-4d0f-b718-0b8acca30cb2)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/21b30304-8d3e-4393-a4f6-a262a81e4632)




sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/bbb02574-5707-4ae3-95ea-c35c0c565d01)




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/5ea7688d-ffab-4276-89d0-77fcf7e0b72b)




sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/e4eb9931-6d0b-4962-a640-4255335d5542)




sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/8e7ca785-1793-4a30-a7dd-4ce69f83e13d)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/9c1203ed-571f-4309-b324-4ae96142d10b)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/d66b2e53-13d0-458b-8959-3dc46556b6b1)



seq 10 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/cc863be0-3c70-4676-889e-7b8e5ef31bb8)




seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/e2cda95f-afd6-4685-850c-f32ffc390955)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/36522126-7998-4c10-a252-d9cb4ab1b8a5)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/758a2bd6-e46c-4409-969e-2ec76634c519)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/dc8a71ee-4128-442e-8499-9ee51853cc99)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/5d16bd3a-bc08-4f93-bcd4-f469f0e07ccc)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/de089387-1d8f-4748-ba00-301f79e01815)



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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/6dac8e6f-f088-4ddc-a348-54b4b343b12d)


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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/dc30f7d0-f25c-4f53-9551-40b20f7ab283)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/383a5e87-b780-4401-b2c0-23b2582bbc56)

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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/868394bc-7a48-4600-abd3-0b9fdd469d0f)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/fea774d2-421a-4fb5-9c4b-547694ad76ff)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/c2a398d1-be7d-435a-bf9f-e78d4975fd57)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/48705666-88e3-4c3b-889e-cde5744b6d61)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/e797204c-f416-49e4-9285-0bf431c48dc9)


gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/b726beb4-a86f-4126-b1c6-7178ed9ff516)

 
gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/9958bc7b-e2cb-4fa5-b362-5226ee85c177)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/5c079df0-12a3-4fad-96eb-c67fbf0d8376)


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/8d8caafe-28de-49a6-bf83-78acf5a518ab)



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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/71bf6f1d-989e-4032-87d8-59d553ebc3a0)

 
ls file1
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/fb9c49e5-9eed-47a7-beb6-7cc9dc9e092e)

echo $?
## OUTPUT 
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/45f51576-bdcf-45b2-bb08-3f083602a7e6)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/8c6c2e38-9a9a-4f4a-b312-65706bc53073)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/c5d79277-70db-461d-9f9c-1007f3ee8972)



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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/59233b03-803e-4ad4-a819-85f8480c413e)


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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/ce0b7605-e464-41bd-b5b5-f0eff2a6cc83)



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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/0c8c0ac7-09cd-4d7f-a694-9699d1b4ca8f)


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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/6a72af4d-87bb-4475-98fb-32eab92a512d)


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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/741dcc06-86c4-411d-a3a5-29af22667823)


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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/1766ec77-a22b-4c92-b48d-11d2c3509dff)


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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/06adef77-0cd7-41b7-b062-6a02e632a684)

 
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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/c9c049b5-6020-4ef5-8e34-5c9ec6b0cacc)

 
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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/ff601f17-f058-4f95-b7dc-c11c16f7eb01)

 
 
 
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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/3092d7e2-727f-40dc-badc-1fbb6fed6961)


 
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
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/d9787591-b646-42cd-80a6-6cdd8aa4dee5)

 
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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/b8cceccc-b148-4cd6-8a0f-5943ad64e3b1)


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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/348c5a48-e966-4477-bbf8-5531303250df)



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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/f8943b37-6a21-4699-a691-4b5ea40b913d)

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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/2cb189a7-5ab5-4a14-9046-d836eb489f81)


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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/c938ad00-7e74-4df6-af65-ce18ec2b85ef)

 
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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/a61eda58-cdff-46d6-87ad-b0c164706299)


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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/941dfd48-5e61-4305-a30b-c69a139f22ac)

 
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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/fc634fbc-bdef-4518-983c-5ea9f02ef1e2)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/8bf01049-f127-4c05-9716-e92deba1762b)



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
$ chmod 755 funcex.sh

$./funcex.sh 

 
$./funcex.sh 1 2
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/68b44d3a-f543-4401-a8c2-d1b8c54d8e2c)


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/2159ce84-735b-4551-a9c1-31ebe771d6c5)

 
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

$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/8766f318-cf18-45f9-b749-559e2f780c31)

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
 ![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/223d5c4b-a8c1-4b07-b7d6-8f76d7b9491c)

 
 
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
![image](https://github.com/Ritika-2706/OS-Linux-commands-Shell-script/assets/93427238/15ced06b-d7f8-4e9b-96c1-308457eaafc4)

 
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
```
Enter the number
 121
 Number is palindrome
 Enter the number
 69
 Number is NOT palindrome

```


# RESULT:
The Commands are executed successfully.
