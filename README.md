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
<img width="531" height="135" alt="image" src="https://github.com/user-attachments/assets/74a6488c-03d0-4cb7-8f83-ddafa7bc013d" />




cat < file2
## OUTPUT
<img width="560" height="131" alt="image" src="https://github.com/user-attachments/assets/b4046180-ef79-4e61-b8c4-18527b33001f" />



# Comparing Files
cmp file1 file2
## OUTPUT

<img width="593" height="51" alt="image" src="https://github.com/user-attachments/assets/b4216991-9399-49bf-bfb8-0803a868879b" />

 
comm file1 file2
 ## OUTPUT

 <img width="597" height="243" alt="image" src="https://github.com/user-attachments/assets/ab62c7c5-d19b-4769-978e-5300bb51f9a5" />


 
diff file1 file2
## OUTPUT

<img width="600" height="242" alt="image" src="https://github.com/user-attachments/assets/d2c235ab-dd9d-464d-9734-777aa9466659" />



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


<img width="611" height="64" alt="image" src="https://github.com/user-attachments/assets/afad5f33-77c3-49fc-8132-c318b8b60899" />





cut -d "|" -f 1 file22
## OUTPUT


<img width="658" height="93" alt="image" src="https://github.com/user-attachments/assets/6b1d9e67-6e50-4e1b-9516-afdc861f19ce" />




cut -d "|" -f 2 file22
## OUTPUT

<img width="651" height="87" alt="image" src="https://github.com/user-attachments/assets/69aea583-f0af-43bf-8082-deec5dba0b63" />



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

<img width="627" height="49" alt="image" src="https://github.com/user-attachments/assets/34cdb065-290e-4942-951c-704289868e8e" />




grep hello newfile 
## OUTPUT

<img width="655" height="51" alt="image" src="https://github.com/user-attachments/assets/63d892d8-942d-41aa-8c8c-864101ffe886" />





grep -v hello newfile 
## OUTPUT

<img width="658" height="52" alt="image" src="https://github.com/user-attachments/assets/91c8292c-97c6-4ee3-9a5b-acf61de8ceac" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="750" height="67" alt="image" src="https://github.com/user-attachments/assets/0fcd2fcb-6715-4dcb-8dda-f5910ab16510" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="776" height="49" alt="image" src="https://github.com/user-attachments/assets/3a34e9af-3e92-493b-a7f7-27e41f1009d6" />





grep -R ubuntu /etc
## OUTPUT

<img width="790" height="174" alt="image" src="https://github.com/user-attachments/assets/cc42e391-baad-4e12-ac2a-efef159377e7" />




grep -w -n world newfile   
## OUTPUT

<img width="694" height="72" alt="image" src="https://github.com/user-attachments/assets/bcc3e972-71ab-44e2-885a-9e50010e731b" />



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

<img width="753" height="69" alt="image" src="https://github.com/user-attachments/assets/4c1a8a3c-7f44-41bb-b22c-fe5fae47b6c9" />




egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="746" height="68" alt="image" src="https://github.com/user-attachments/assets/34b1a93c-8026-4490-9df5-6434d891f0d8" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="796" height="79" alt="image" src="https://github.com/user-attachments/assets/3a9ee668-0bf2-4c5a-8724-5fcf819df014" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="704" height="50" alt="image" src="https://github.com/user-attachments/assets/4241a4a6-fe66-436c-8df2-333419d59fbb" />




egrep '(world$)' newfile 
## OUTPUT

<img width="710" height="74" alt="image" src="https://github.com/user-attachments/assets/34c96f2d-7abc-4278-8645-3ed9d2128485" />




egrep '(World$)' newfile 
## OUTPUT

<img width="690" height="70" alt="image" src="https://github.com/user-attachments/assets/f23c5766-0963-4600-a051-de6e69f9732d" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="749" height="92" alt="image" src="https://github.com/user-attachments/assets/49a3aee5-4da1-4c0b-935e-db072d9e7e4c" />




egrep '[1-9]' newfile 
## OUTPUT

<img width="673" height="54" alt="image" src="https://github.com/user-attachments/assets/a6e6b29a-e762-4ad8-a7ad-6c4fcddff57b" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="743" height="52" alt="image" src="https://github.com/user-attachments/assets/0bc19a20-769a-4340-8a84-319ff4d3155a" />



egrep 'Linux.*World' newfile 
## OUTPUT

<img width="747" height="53" alt="image" src="https://github.com/user-attachments/assets/cdc7d4d0-cf78-452c-8a37-57fc035889ad" />



egrep l{2} newfile
## OUTPUT

<img width="636" height="73" alt="image" src="https://github.com/user-attachments/assets/23429044-86d9-45fc-8f17-99cfc2113c61" />




egrep 's{1,2}' newfile
## OUTPUT 

<img width="667" height="92" alt="image" src="https://github.com/user-attachments/assets/1b1514e8-9b38-4494-bb00-486b76097ac9" />



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

<img width="1026" height="47" alt="image" src="https://github.com/user-attachments/assets/c68203f7-dfcd-4b7c-9a5d-5b15bfd2bf94" />




sed -n -e '$p' file23
## OUTPUT

<img width="1030" height="46" alt="image" src="https://github.com/user-attachments/assets/36e6030f-d44c-4f52-bf40-c42d518fb4fd" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1031" height="180" alt="image" src="https://github.com/user-attachments/assets/7bc390f6-6d77-4693-8a56-6af2b8e7649f" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1032" height="182" alt="image" src="https://github.com/user-attachments/assets/5c5464ef-2b74-4c79-b880-ca3f94ff75be" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1037" height="182" alt="image" src="https://github.com/user-attachments/assets/300622c8-6e64-46bf-876f-d38445b6b39f" />




sed -n -e '1,5p' file23
## OUTPUT

<img width="995" height="123" alt="image" src="https://github.com/user-attachments/assets/6fd7c49e-0108-47fb-916b-47950991881a" />




sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1022" height="91" alt="image" src="https://github.com/user-attachments/assets/295d442d-a936-4e3f-9569-3b7b96f230e2" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1035" height="61" alt="image" src="https://github.com/user-attachments/assets/81cf6682-7dac-4d8e-ab58-d1b6dd203c32" />




seq 10 
## OUTPUT

<img width="945" height="249" alt="image" src="https://github.com/user-attachments/assets/cca4b5e0-54b5-42ff-be03-2ee7a4d15562" />




seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1021" height="85" alt="image" src="https://github.com/user-attachments/assets/c758f5e7-c6d8-4364-bfb6-d94439ecb55b" />




seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1037" height="89" alt="image" src="https://github.com/user-attachments/assets/02676cce-12b4-4282-9a62-9a2e3fece3cf" />




seq 3 | sed '2a hello'
## OUTPUT

<img width="1024" height="101" alt="image" src="https://github.com/user-attachments/assets/95da05b8-f566-4525-abab-d4810e2d022a" />




seq 2 | sed '2i hello'
## OUTPUT

<img width="1034" height="95" alt="image" src="https://github.com/user-attachments/assets/5ede078e-2779-4a62-a59b-c50a64819f08" />



seq 10 | sed '2,9c hello'
## OUTPUT

<img width="1035" height="97" alt="image" src="https://github.com/user-attachments/assets/e714b8e9-a474-4383-bb42-bb256a1c0ca8" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1038" height="81" alt="image" src="https://github.com/user-attachments/assets/1f69c98c-f860-4bef-a73c-2aee61fa5c23" />




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

<img width="1035" height="82" alt="image" src="https://github.com/user-attachments/assets/9b322179-faa8-4e6c-967a-7a68cfd5f97f" />



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

<img width="982" height="142" alt="image" src="https://github.com/user-attachments/assets/7f9624fe-acbd-4099-b605-536697295271" />




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

 <img width="1028" height="85" alt="image" src="https://github.com/user-attachments/assets/e334f6af-7dff-40c8-aaf1-f0f543a092b7" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1020" height="77" alt="image" src="https://github.com/user-attachments/assets/f38a8112-79b5-4e9d-a5c7-93c98066fe55" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="1034" height="428" alt="image" src="https://github.com/user-attachments/assets/eee02e28-40ba-4fe3-96ac-3ac280ac7bd1" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1031" height="796" alt="image" src="https://github.com/user-attachments/assets/e9e75a73-55d3-47b0-b42d-fb81c139cbba" />



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

echo $?
## OUTPUT 
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


# RESULT:
The Commands are executed successfully.
