# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
```
Developed by: Naveenkumar M
Register number: 212224230182

```
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
s.n. dasguptacat > file1
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla < file
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="276" height="147" alt="image" src="https://github.com/user-attachments/assets/daca4092-20cb-4fa6-934d-41238e826043" />



cat < file2
## OUTPUT
<img width="314" height="169" alt="image" src="https://github.com/user-attachments/assets/25546b91-03b2-4c2f-8d7b-c9d79b54ced4" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="358" height="77" alt="image" src="https://github.com/user-attachments/assets/f37ab6a3-7f30-44f2-8d79-74d0a577475e" />

 
comm file1 file2
 ## OUTPUT
<img width="352" height="229" alt="image" src="https://github.com/user-attachments/assets/6a4ef481-97f1-42ba-90bf-64a00d797e1c" />

 
diff file1 file2
## OUTPUT
<img width="355" height="276" alt="image" src="https://github.com/user-attachments/assets/9d862dbf-8b53-4f12-816a-0c00575c2bf5" />


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
<img width="331" height="104" alt="image" src="https://github.com/user-attachments/assets/475bbeb2-8aaf-4fe4-9db8-b9cf97db7d43" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="313" height="129" alt="image" src="https://github.com/user-attachments/assets/2d03cb8c-cc28-4e07-aa50-ef318c5d7a2b" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="343" height="126" alt="image" src="https://github.com/user-attachments/assets/8bdda26f-e8df-49f2-8332-bee181719dca" />


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
<img width="321" height="69" alt="image" src="https://github.com/user-attachments/assets/9300788f-577f-4f54-bf1c-4f1687672eff" />



grep hello newfile 
## OUTPUT
<img width="281" height="76" alt="image" src="https://github.com/user-attachments/assets/6be342ea-49bd-4d3d-b864-edcfaeb7eb4b" />


grep -v hello newfile 
## OUTPUT
<img width="300" height="75" alt="image" src="https://github.com/user-attachments/assets/53ba8d75-61c6-41bc-83c2-faaf968ed916" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="376" height="99" alt="image" src="https://github.com/user-attachments/assets/51b43822-8e77-4e1b-9b8c-6311beddca15" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="413" height="78" alt="image" src="https://github.com/user-attachments/assets/40584109-0f23-425d-a7ca-01063cbb66b4" />




grep -R ubuntu /etc
## OUTPUT
<img width="803" height="595" alt="image" src="https://github.com/user-attachments/assets/c5c536dd-af5e-43ac-84f5-8bdd38ce75ac" />



grep -w -n world newfile   
## OUTPUT
<img width="330" height="93" alt="image" src="https://github.com/user-attachments/assets/ff6046a7-ea94-4218-b500-8950c0fc9ad0" />


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
<img width="379" height="103" alt="image" src="https://github.com/user-attachments/assets/3f7794d2-bc33-4b11-b2b0-faee3b92b491" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="359" height="100" alt="image" src="https://github.com/user-attachments/assets/934403fb-17a4-4c3d-9b90-7ded7d29164c" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="406" height="101" alt="image" src="https://github.com/user-attachments/assets/684610ca-7e0b-4c97-ad8d-055baf13be6c" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="339" height="75" alt="image" src="https://github.com/user-attachments/assets/fc12b430-5b57-41ed-8303-c56c15c7afad" />



egrep '(world$)' newfile 
## OUTPUT
<img width="318" height="101" alt="image" src="https://github.com/user-attachments/assets/d373e63d-8f26-4a07-890f-b3ae3b1b170f" />



egrep '(World$)' newfile 
## OUTPUT
<img width="321" height="71" alt="image" src="https://github.com/user-attachments/assets/5a6a083f-8bbf-493d-9811-e6fee504eb12" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="395" height="127" alt="image" src="https://github.com/user-attachments/assets/37dbf443-9b1d-4075-a324-8519eb74b77c" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="302" height="75" alt="image" src="https://github.com/user-attachments/assets/e27e4269-9721-40ed-a759-5c95beff619b" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="377" height="77" alt="image" src="https://github.com/user-attachments/assets/a998626d-d93e-4856-9892-d3e76b42414a" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="405" height="76" alt="image" src="https://github.com/user-attachments/assets/202d538c-3649-4a77-abdc-ab0d186c659f" />


egrep l{2} newfile
## OUTPUT
<img width="315" height="104" alt="image" src="https://github.com/user-attachments/assets/1f19dd8f-d78a-4e46-bef3-3174d87651cd" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="337" height="129" alt="image" src="https://github.com/user-attachments/assets/33af2d03-a67f-42b5-8855-017dacd8e57f" />


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
<img width="321" height="79" alt="image" src="https://github.com/user-attachments/assets/080bc2b8-a9ae-4a3a-9998-993c85bd24f4" />



sed -n -e '$p' file23
## OUTPUT
<img width="303" height="76" alt="image" src="https://github.com/user-attachments/assets/92075b1b-4f88-4ec5-9ead-4f181aad36c3" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="353" height="252" alt="image" src="https://github.com/user-attachments/assets/0b8399a3-a5a5-476a-adb9-3819e8b85c68" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="380" height="248" alt="image" src="https://github.com/user-attachments/assets/c6a971ff-b1ae-4cc0-91db-59816e8cfaa0" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="404" height="256" alt="image" src="https://github.com/user-attachments/assets/fd77db3f-d6b1-43c8-8630-5a78a65e07fb" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="337" height="176" alt="image" src="https://github.com/user-attachments/assets/aa687eeb-3c31-4981-8aa1-00901e2b24d5" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="341" height="129" alt="image" src="https://github.com/user-attachments/assets/263bb90d-d97a-4950-93be-dc96687458e0" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="376" height="100" alt="image" src="https://github.com/user-attachments/assets/0222ea17-a649-4ebb-a160-f7985ded5aa8" />



seq 10 
## OUTPUT
<img width="325" height="297" alt="image" src="https://github.com/user-attachments/assets/d2beb469-a934-43e2-a985-d46d960102b4" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="304" height="129" alt="image" src="https://github.com/user-attachments/assets/5fa5a53d-ed78-4cbd-884e-0cad6a7e9d81" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="353" height="133" alt="image" src="https://github.com/user-attachments/assets/99ad00f2-49b1-457b-8982-6d239844d0bf" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="342" height="148" alt="image" src="https://github.com/user-attachments/assets/480b6fe8-b1ef-4061-bdfb-34e275e3dfd1" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="306" height="129" alt="image" src="https://github.com/user-attachments/assets/125e303e-5163-4b04-a184-a2f99422eae3" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="336" height="131" alt="image" src="https://github.com/user-attachments/assets/bcad1695-d9da-4f43-a652-82e8b668f3e2" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="360" height="122" alt="image" src="https://github.com/user-attachments/assets/b3ff61dc-3393-4687-9a39-ce3756227b07" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="391" height="125" alt="image" src="https://github.com/user-attachments/assets/5b95f98f-461d-4f60-be79-7e91e37961fa" />


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
<img width="327" height="180" alt="image" src="https://github.com/user-attachments/assets/b8022cbd-5e5b-4c6e-99b2-6ce30ea44a94" />



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
<img width="329" height="175" alt="image" src="https://github.com/user-attachments/assets/d811fc50-b117-42e8-be2f-1eb9ed7e6206" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="420" height="250" alt="image" src="https://github.com/user-attachments/assets/0dd4449e-7eed-472f-aa06-7a47b3744fd5" />


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
<img width="338" height="127" alt="image" src="https://github.com/user-attachments/assets/86d318b2-5933-4d16-940b-ae3dd8cc0d0c" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="471" height="126" alt="image" src="https://github.com/user-attachments/assets/d9676f27-9a9a-4323-a052-34673cc52df7" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="496" height="783" alt="image" src="https://github.com/user-attachments/assets/ca1d2efe-3728-4c8e-add8-fc357445c27e" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="652" height="380" alt="image" src="https://github.com/user-attachments/assets/2c327c8f-b3ce-422b-80e0-40770c8aa7ea" />



tar -xvf backup.tar
## OUTPUT
<img width="652" height="268" alt="image" src="https://github.com/user-attachments/assets/8ca17e12-a9c4-4a8a-8b58-2e6ac5226b3d" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="655" height="229" alt="image" src="https://github.com/user-attachments/assets/d79b8ebe-12df-4afb-a323-0e0f68177110" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="653" height="177" alt="image" src="https://github.com/user-attachments/assets/cf03cc45-71fc-4c64-950c-1580fad8d4d1" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="549" height="176" alt="image" src="https://github.com/user-attachments/assets/b14bf729-9313-42d4-aaf9-8d107dbe380c" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="342" height="123" alt="image" src="https://github.com/user-attachments/assets/c8fd07d5-f850-4e7d-995f-dcc8c54325e7" />



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

 
ls file1
## OUTPUT
<img width="491" height="86" alt="image" src="https://github.com/user-attachments/assets/471fb678-4047-495b-99ac-e0ff1157faea" />


echo $?
## OUTPUT 

<img width="487" height="72" alt="image" src="https://github.com/user-attachments/assets/41f98b69-960a-4b9c-9dcb-dc7db0085c85" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="493" height="87" alt="image" src="https://github.com/user-attachments/assets/f8c35032-5f86-464b-a7d5-f9ceeace8ff3" />

abcd
 
echo $?
 ## OUTPUT
 <img width="493" height="87" alt="image" src="https://github.com/user-attachments/assets/f8c35032-5f86-464b-a7d5-f9ceeace8ff3" />

 
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
<img width="623" height="317" alt="image" src="https://github.com/user-attachments/assets/b0248b92-5463-4e8e-9a38-39b630e78121" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="684" height="445" alt="image" src="https://github.com/user-attachments/assets/f8fe0368-130f-417e-a015-65f5c4d3cd34" />


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
<img width="779" height="393" alt="image" src="https://github.com/user-attachments/assets/df201542-ed14-40e5-81b9-610cb5b4de86" />

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
<img width="647" height="704" alt="image" src="https://github.com/user-attachments/assets/2a8f8e5a-fe50-48b7-bb9e-e08a6a9a4a5c" />



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
<img width="718" height="531" alt="image" src="https://github.com/user-attachments/assets/31de1655-196e-454c-942d-cd675d532082" />

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
<img width="869" height="657" alt="image" src="https://github.com/user-attachments/assets/f07ac986-428a-4fb1-93f4-fe5387c42f4a" />

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
<img width="595" height="621" alt="image" src="https://github.com/user-attachments/assets/e9d65a2a-9d9a-4d0f-b957-5062382576d5" />


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
<img width="734" height="360" alt="image" src="https://github.com/user-attachments/assets/ea8aedd0-ae78-4ff8-a01f-2157a3a4ebc0" />

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

## Output
<img width="582" height="465" alt="image" src="https://github.com/user-attachments/assets/56543979-0f5a-42d6-8c96-cde41f04116a" />

 
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
 ## Output
 <img width="566" height="580" alt="image" src="https://github.com/user-attachments/assets/341460ea-2618-40a9-b771-bcaf767c7c3a" />

 
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
 <img width="481" height="471" alt="image" src="https://github.com/user-attachments/assets/90d11c89-af43-4192-8b98-6b94f6173976" />

 
 
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
## Output

 <img width="725" height="426" alt="image" src="https://github.com/user-attachments/assets/e43604bf-3e59-47bf-926a-a963f671f7bc" />

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
## Output
<img width="552" height="355" alt="image" src="https://github.com/user-attachments/assets/563fc83f-6268-4f7c-98d6-e2bfba12a58d" />

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
 ## Output
 <img width="727" height="346" alt="image" src="https://github.com/user-attachments/assets/d9394fa5-76b4-46a0-ad56-1dd6ce63c1d8" />

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
## Output

 <img width="708" height="429" alt="image" src="https://github.com/user-attachments/assets/12cb9aeb-1630-44cb-81cd-ec04070a08c1" />

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
<img width="800" height="439" alt="image" src="https://github.com/user-attachments/assets/6942fae0-0c4b-485d-b383-4dce2156511e" />

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
<img width="651" height="489" alt="image" src="https://github.com/user-attachments/assets/9c4c6b21-ad5e-414c-a1dc-15971d14a33e" />


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
<img width="596" height="397" alt="image" src="https://github.com/user-attachments/assets/48dd85d9-d90f-4822-9097-59e8ca281561" />

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
<img width="721" height="410" alt="image" src="https://github.com/user-attachments/assets/71495d5e-bfb9-476b-9278-24aa222bcf90" />

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
<img width="742" height="709" alt="image" src="https://github.com/user-attachments/assets/8a80268c-06f0-4031-8fb2-65a5c41459ec" />

 
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
<img width="729" height="502" alt="image" src="https://github.com/user-attachments/assets/66d5babb-615a-4e68-a850-027fdc0df354" />

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
<img width="893" height="532" alt="image" src="https://github.com/user-attachments/assets/d7d0c3df-d145-4987-8f0d-e31fe4a3851d" />
 
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
<img width="804" height="316" alt="image" src="https://github.com/user-attachments/assets/12671bf8-2b4b-4f9a-af7c-3f6e07382658" />


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
<img width="615" height="307" alt="image" src="https://github.com/user-attachments/assets/de9c838f-39c4-4108-ab54-35c2f5af18ca" />




 
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

 
 ./funcex.sh 1 2
## OUTPUT
<img width="706" height="536" alt="image" src="https://github.com/user-attachments/assets/e9055438-5913-4c65-81b7-c4e91e662311" />

 
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
<img width="420" height="355" alt="image" src="https://github.com/user-attachments/assets/dedc8f67-01f1-4404-ae30-f2bb3dd74812" />

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
<img width="608" height="450" alt="image" src="https://github.com/user-attachments/assets/5d9e3528-475f-4482-900a-b09f6c21f464" />

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
<img width="684" height="685" alt="image" src="https://github.com/user-attachments/assets/f0b44043-d980-4a59-967b-61d789c18991" />

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
<img width="667" height="420" alt="image" src="https://github.com/user-attachments/assets/5b91aa1e-29a2-4fad-9906-7763d63e3bb2" />

 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0CHMOD CHMOD  ]
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
<img width="528" height="262" alt="image" src="https://github.com/user-attachments/assets/accaa5ab-7cb9-48eb-95fa-624f015986d5" />


# RESULT:
The Commands are executed successfully.
