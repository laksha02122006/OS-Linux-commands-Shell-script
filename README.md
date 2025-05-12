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

![image](https://github.com/user-attachments/assets/e7a80412-7118-41b7-8dad-b0de686cdf60)


cat < file2
## OUTPUT


![image](https://github.com/user-attachments/assets/a65a9c58-0afc-40bb-959e-61af2ee8e651)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![image](https://github.com/user-attachments/assets/25b09014-3715-4a1d-a66c-5845c61ef595)

comm file1 file2
 ## OUTPUT

![image](https://github.com/user-attachments/assets/0ce763c6-5898-4f45-9549-2ff9afa0fe7a)

 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/1e9a5e5b-21c3-4f9f-8e45-7b013819d625)


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


![image](https://github.com/user-attachments/assets/aaa456ca-8623-4e2f-bd57-d070e2ccc5a8)



cut -d "|" -f 1 file22
## OUTPUT


![image](https://github.com/user-attachments/assets/6d5db081-2070-4371-a37b-359b44ac5375)


cut -d "|" -f 2 file22
## OUTPUT


![image](https://github.com/user-attachments/assets/d9d48134-163d-4911-a8e3-e9b75f46adbe)

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


![image](https://github.com/user-attachments/assets/b773e40d-571a-4ab8-9f71-e3a1796a785f)


grep hello newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/52f1da27-6e97-4132-a836-579311bd3d69)



grep -v hello newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/3d012d96-fc09-4b04-a7c1-d6503f2ceac9)


cat newfile | grep -i "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/ad6449f9-2f28-4c96-9c8f-a78e8ce00aa8)



cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/a361c03d-be32-4915-8881-d5188045a8a4)



grep -R ubuntu /etc
## OUTPUT


![image](https://github.com/user-attachments/assets/48771c95-6b5e-40d5-8f0a-d342ec0edf2c)


grep -w -n world newfile   
## OUTPUT


![image](https://github.com/user-attachments/assets/6bacbe98-e7ce-4f58-ac5f-d7946a0c4730)

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


![image](https://github.com/user-attachments/assets/11ab609c-dee0-4850-951d-3587ff62296d)


egrep -w '(H|h)ello' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/b8431b80-226a-4a64-8119-19e5def1d51a)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/e2b44184-1e04-4f49-acee-e31973f396c8)



egrep '(^hello)' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/ff86985d-725c-4df9-a318-811239200eae)


egrep '(world$)' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/3d9f2219-84e9-4b10-a3a2-8ccdc8a1cec2)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/0aa2d266-da1a-481c-8268-5d5a62eb473d)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/6f04aff3-fc5f-40e2-baf8-3c6fcc97e6f9)



egrep '[1-9]' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/f14a438a-974a-4de1-b94c-7d6198afb620)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b6693fd5-9756-49e1-a35e-4da158116d6c)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/a5039a1b-93d2-4b24-94f7-c5aedcf99915)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/d350e3e3-420d-491b-bbe5-94400a837f4b)



egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/c58c50ea-ac1d-419f-8049-b91f2ecbd4c5)


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


![image](https://github.com/user-attachments/assets/4f9cb34e-bb39-4e97-a85a-1536c5177e44)


sed -n -e '$p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/bf96c579-39de-47d9-a62f-0808a2b9bfa1)


sed  -e 's/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/b44b520e-836a-4b85-b68e-e11e069ba259)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/78b48b2a-99a3-4d5f-bc12-2e3c9ef923b1)


sed  '/tom/s/5000/6000/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/3937a2ea-7348-4531-87ed-b952275328bc)


sed -n -e '1,5p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/7186eef0-06a0-4710-82fa-5bc9a0f626e1)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/e4d47735-d4db-4887-9310-3dbd43343e11)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/cbf9d9cc-9912-41e7-9218-f25ed04a578b)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/0f337851-6ada-4db2-8b8d-67a4abd8c7d1)



seq 10 | sed -n '4,6p'
## OUTPUT


![image](https://github.com/user-attachments/assets/5090e71a-7a4a-4058-b2af-011ce94ca249)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/c3b66430-35de-44f2-91c0-f25a32ac6c26)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/d1c1638e-78f6-49fd-ab0f-ba341b6b1f11)



seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/43f3f7fe-d5a2-4e3e-afef-d759b768a52e)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/09e94b55-66bc-4ddf-bb99-02d74ed35bba)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/d22d7b2a-d58b-46ca-8789-fdcfc31d8f01)


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

![image](https://github.com/user-attachments/assets/a1af1c52-5e0f-4646-98e8-ba956daa4e23)


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

![image](https://github.com/user-attachments/assets/f10c8d27-c53c-4f02-94a3-dcd4662530b1)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/user-attachments/assets/c02d1302-becb-47f5-8fd2-bb890c461e94)

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


![image](https://github.com/user-attachments/assets/036bf907-76c0-42e0-8d9f-a7e031e3bc78)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![image](https://github.com/user-attachments/assets/1cee4af4-8ed2-492b-b31e-dcf4505d2198)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


![image](https://github.com/user-attachments/assets/4a2bac11-c1a3-4d52-bc78-b83c6aef41c3)

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/de259800-46ba-42ff-bea8-f9f7505ff76a)


tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/8f870a1a-c754-4907-864b-a54ee73f2589)

gzip backup.tar

ls .gz
## OUTPUT

 ![image](https://github.com/user-attachments/assets/13152e0e-8314-4350-a07a-1b77cf7223ac)

gunzip backup.tar.gz
## OUTPUT


 ![image](https://github.com/user-attachments/assets/616e0339-ff35-4d10-8300-4aecb8be489a)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/2b2a9541-b171-4140-a8ed-202630a0d7a2)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


![image](https://github.com/user-attachments/assets/fb359425-74db-41ff-9a31-1c2d2ef2f876)

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

![image](https://github.com/user-attachments/assets/33b53d8c-25a9-4d69-b287-5a77eefca4d5)

 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/02a7691a-881b-4a1b-87e9-af01cd199adb)

echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/2f8aa6e4-519a-426e-85d2-5e36a4c7a2de)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 ![image](https://github.com/user-attachments/assets/d96d2f31-83f3-4de5-b065-c1134e5cced7)

abcd
 
echo $?
 ## OUTPUT


![image](https://github.com/user-attachments/assets/1558edd3-a135-4f60-b6e0-f3d105225c25)

 
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

![image](https://github.com/user-attachments/assets/58a7b716-ae99-4b7a-aa85-7cc40fcb82ce)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


![image](https://github.com/user-attachments/assets/b457376f-6c1f-414a-a9cf-35df6344c191)

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

![image](https://github.com/user-attachments/assets/cb532c20-b377-40a6-82ec-0af016d9d05c)

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


![image](https://github.com/user-attachments/assets/46091b0b-0b18-4c99-bad8-4d15ece59a3b)


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

![image](https://github.com/user-attachments/assets/f81b0a74-071b-4f0e-b980-360ac24f7d79)

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

![image](https://github.com/user-attachments/assets/8f9799ee-2c90-4609-b762-fa2cc25bbe57)

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

![image](https://github.com/user-attachments/assets/7f7e9160-1068-4ebd-9319-ff9f05acbd7e)


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

![image](https://github.com/user-attachments/assets/6203e106-a3e4-41eb-9f54-90b6d5eeda6c)

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

![image](https://github.com/user-attachments/assets/7dfb1a3e-259b-4728-af48-c4fd00fbccf1)

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

![image](https://github.com/user-attachments/assets/0aebb38e-039d-4c43-8b85-f5e9043d2599)


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

![image](https://github.com/user-attachments/assets/7ae75eae-d021-422f-ad8c-a0da98123fbb)

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

![image](https://github.com/user-attachments/assets/a60a2de7-d52a-4419-9ce7-3a8a12962a56)

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


 ![image](https://github.com/user-attachments/assets/ec620af5-eca2-42b0-a0a1-1c074402b9ce)

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

![image](https://github.com/user-attachments/assets/d5ecb3ea-f58d-4130-b18c-5828cdb8ad2a)

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

 ![image](https://github.com/user-attachments/assets/386f80cd-a7fb-46ad-b2fb-15c08c245f0e)

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

![image](https://github.com/user-attachments/assets/c2d90e3c-aca2-4d7d-8fd6-defe16a8d769)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


![image](https://github.com/user-attachments/assets/da2dec1c-f929-480f-891d-c71da9fa226c)


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

![image](https://github.com/user-attachments/assets/90b9ef87-804e-4b6c-8e1a-2c14f9d705bc)

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

![image](https://github.com/user-attachments/assets/91f732d4-9043-489d-9680-75f945a8a7bb)

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

![image](https://github.com/user-attachments/assets/23c2e3b6-419c-45a2-ba31-cbb10edbf04b)

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

![image](https://github.com/user-attachments/assets/62fe2233-de5c-4cf8-af60-8df4817b846b)

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

![image](https://github.com/user-attachments/assets/93c2176b-b1ee-41b4-b5e2-abb76a16da40)

 
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

![image](https://github.com/user-attachments/assets/8fb7d95b-f2f4-4c56-9ac2-6cd22fa7897b)


# RESULT:
The Commands are executed successfully.
