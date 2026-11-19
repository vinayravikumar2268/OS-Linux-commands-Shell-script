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
<img width="353" height="84" alt="image" src="https://github.com/user-attachments/assets/2622f5eb-e5f5-4ad2-a378-0c31bd83a54c" />



cat < file2
## OUTPUT
<img width="248" height="99" alt="image" src="https://github.com/user-attachments/assets/8ea609db-ed44-403c-b125-5600a8f2c4f9" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="282" height="179" alt="image" src="https://github.com/user-attachments/assets/64d629eb-5931-4e40-8841-d28f4d4f98c8" />
 
comm file1 file2
 ## OUTPUT


 
diff file1 file2
## OUTPUT
<img width="296" height="131" alt="image" src="https://github.com/user-attachments/assets/78226060-f444-4d1f-8eb1-8975b1195a55" />


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
<img width="294" height="306" alt="image" src="https://github.com/user-attachments/assets/9d3729d9-f637-4c19-a84d-c74bfbe1baa6" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="286" height="118" alt="image" src="https://github.com/user-attachments/assets/e1c0203d-1de0-4eae-80d2-1a93bcf9c0be" />



cut -d "|" -f 2 file22
## OUTPUT



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
<img width="252" height="69" alt="image" src="https://github.com/user-attachments/assets/2eb976f4-093e-4ca5-9993-18e4daa50383" />



grep hello newfile 
## OUTPUT
<img width="257" height="86" alt="image" src="https://github.com/user-attachments/assets/2eb1e615-f535-4684-ae8e-695baebb91e9" />




grep -v hello newfile 
## OUTPUT
<img width="293" height="83" alt="image" src="https://github.com/user-attachments/assets/b63a376e-a5ea-47fb-9a11-e181a6b500a5" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="369" height="111" alt="image" src="https://github.com/user-attachments/assets/067f319d-6c83-465c-815c-254c62d4c0c1" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="399" height="75" alt="image" src="https://github.com/user-attachments/assets/7f6dea60-d0b4-4639-aa37-536522b8793e" />


grep -R ubuntu /etc
## OUTPUT




grep -w -n world newfile   
## OUTPUT
<img width="333" height="91" alt="image" src="https://github.com/user-attachments/assets/926ea01b-6d4b-43cf-9f17-b898247b7672" />


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
<img width="379" height="115" alt="image" src="https://github.com/user-attachments/assets/e507225d-821e-4cf6-a823-47dec294c24a" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="372" height="100" alt="image" src="https://github.com/user-attachments/assets/efabc964-4e48-4087-bcaf-605f758c9895" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="399" height="116" alt="image" src="https://github.com/user-attachments/assets/e051a99b-74cc-4dcb-9cea-00fd062b0128" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="317" height="85" alt="image" src="https://github.com/user-attachments/assets/7f83cc6b-5781-4faa-be97-59ca12959d1f" />



egrep '(world$)' newfile 
## OUTPUT
<img width="334" height="100" alt="image" src="https://github.com/user-attachments/assets/0941136c-2af7-47ca-8fd2-d03879a35f51" />



egrep '(World$)' newfile 
## OUTPUT
<img width="319" height="100" alt="image" src="https://github.com/user-attachments/assets/7dce1057-271b-4e6a-8fa6-cc7b4934334f" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="360" height="137" alt="image" src="https://github.com/user-attachments/assets/e72d399b-6b51-4fdd-bbf7-24e2686e7d35" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="289" height="87" alt="image" src="https://github.com/user-attachments/assets/8a046a06-8fa1-4247-bd0d-c28fbc9bd47b" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="360" height="79" alt="image" src="https://github.com/user-attachments/assets/d3c94bdb-bb0e-45e2-a9dc-872e0b248cd1" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="369" height="81" alt="image" src="https://github.com/user-attachments/assets/eaa073b3-471f-4870-ba60-54592104c59e" />


egrep l{2} newfile
## OUTPUT
<img width="280" height="109" alt="image" src="https://github.com/user-attachments/assets/0367af4c-fa85-4049-b216-413ab5403034" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="304" height="133" alt="image" src="https://github.com/user-attachments/assets/96df5654-c463-4dbf-aab4-3fc8dc6dae7a" />



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
<img width="310" height="81" alt="image" src="https://github.com/user-attachments/assets/27204532-862a-4ce2-af08-e92c5ef73eab" />



sed -n -e '$p' file23
## OUTPUT
<img width="282" height="82" alt="image" src="https://github.com/user-attachments/assets/b2ff5324-ab04-4002-9ee9-091494abdec2" />





sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="360" height="247" alt="image" src="https://github.com/user-attachments/assets/06e365fd-b9a4-4afc-8ca0-5590c4788570" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="344" height="187" alt="image" src="https://github.com/user-attachments/assets/0436536c-7fc9-40f3-affc-2a0056970b25" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="344" height="187" alt="image" src="https://github.com/user-attachments/assets/96790ff6-a1f3-4721-83d3-e3be4e52806c" />






sed -n -e '1,5p' file23
## OUTPUT
<img width="387" height="249" alt="image" src="https://github.com/user-attachments/assets/b5bc95ed-5bdf-4525-a35d-ff89080d4747" />





sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="341" height="135" alt="image" src="https://github.com/user-attachments/assets/628305bf-c426-4f4c-8eae-9924102dc7fc" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="384" height="112" alt="image" src="https://github.com/user-attachments/assets/c1577fab-aa4f-4304-be4a-474ea9e875b3" />



seq 10 
## OUTPUT
<img width="213" height="311" alt="image" src="https://github.com/user-attachments/assets/fe72d0bf-f048-4793-ac82-4649f5edf1f3" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="287" height="140" alt="image" src="https://github.com/user-attachments/assets/f0aa1a60-5ebd-4bab-93a7-2e28948a919f" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="310" height="142" alt="image" src="https://github.com/user-attachments/assets/76dac0ba-9903-418b-9128-6a188e60b8cd" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="295" height="164" alt="image" src="https://github.com/user-attachments/assets/7fa18a35-d699-4513-b566-df173638e228" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="305" height="121" alt="image" src="https://github.com/user-attachments/assets/0abb241e-650c-4020-8028-26a66bbd61d3" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="354" height="129" alt="image" src="https://github.com/user-attachments/assets/d6574dcd-50cb-470e-9cc1-0a94e473e6b8" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="455" height="168" alt="image" src="https://github.com/user-attachments/assets/35b9715a-92ed-4b44-9335-6de0cfa3602b" />

<img width="389" height="135" alt="image" src="https://github.com/user-attachments/assets/b3d1606d-11e9-415c-8a7e-601300309662" />








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
<img width="311" height="180" alt="image" src="https://github.com/user-attachments/assets/ba2b30b3-6fba-40f5-9197-2e0da0232103" />




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
<img width="305" height="184" alt="image" src="https://github.com/user-attachments/assets/cfa032f7-4b69-4514-8112-df073fe78357" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="443" height="250" alt="image" src="https://github.com/user-attachments/assets/93f51cf1-7442-4889-970a-229d95db584b" />


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
<img width="340" height="134" alt="image" src="https://github.com/user-attachments/assets/4eaf19e6-0278-402e-83d8-06738c68d566" />







 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="483" height="136" alt="image" src="https://github.com/user-attachments/assets/a72fbe01-1a5b-48a4-9e7f-751641883e5a" />







#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="521" height="538" alt="image" src="https://github.com/user-attachments/assets/caf6c795-fd98-4215-8fd8-a2eeb9c08a41" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="533" height="110" alt="image" src="https://github.com/user-attachments/assets/202a4274-c701-4be7-8775-30408294c585" />


tar -xvf backup.tar
## OUTPUT
<img width="524" height="98" alt="433121309-4b8c5a7a-e2cb-4193-8598-49dd146ae354" src="https://github.com/user-attachments/assets/fcb9ef16-dd87-46c9-bdd6-7ef51156f125" />



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="323" height="78" alt="433121485-173f2389-dcf2-4000-b666-b177dc48a719" src="https://github.com/user-attachments/assets/c91e37e6-3341-43ec-9cb2-6c71d7ad1155" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="265" height="160" alt="433121538-01a793d4-0e77-4281-a74d-bd362ade6bef" src="https://github.com/user-attachments/assets/d14d0bbe-25ac-4274-8320-2f7781ce1343" />

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
<img width="233" height="74" alt="433121659-de2059a7-76e6-4545-ae0b-9a2b75da7c6a" src="https://github.com/user-attachments/assets/22da2605-bac8-4cde-8949-bd3218506c2a" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="405" height="195" alt="433121736-4f660d09-654d-4517-9741-1051063c42ab" src="https://github.com/user-attachments/assets/1603a97e-cf5b-4d03-8ca5-f553580bc6fe" />

abcd
 
echo $?
 ## OUTPUT

<img width="255" height="74" alt="433121760-7e3996f4-ba60-48ac-9126-77dfd087232e" src="https://github.com/user-attachments/assets/989ab653-6440-4984-b426-13fffa8c1ca1" />

 
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

<img width="523" height="119" alt="433121872-ff4538ee-5b42-40da-8c50-a6944b7d1400" src="https://github.com/user-attachments/assets/54a86259-ef66-4fc2-8cdd-a1119595b37f" />
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
<img width="481" height="80" alt="433122112-09c5df08-b44f-4794-97bd-ea9d5f2c3c49" src="https://github.com/user-attachments/assets/813e4871-94ea-4965-b930-bb49dc9213ff" />

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
<img width="400" height="85" alt="433122128-254d4db1-d953-46b4-9991-89688f8eff0a" src="https://github.com/user-attachments/assets/f97383f6-ce90-43de-80de-6b51502f78e5" />



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
<img width="379" height="136" alt="433122630-d4b6e094-98ff-4f14-a0ac-edac0dbfdb2f" src="https://github.com/user-attachments/assets/86456a4f-0dcb-4a67-a860-494469c90dff" />



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
<img width="372" height="137" alt="433122742-e9dff7b1-4c1a-4757-8157-3ad38e0687fb" src="https://github.com/user-attachments/assets/2b4a22b2-26ea-4df0-a653-8d5959d8576f" />

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
<img width="515" height="223" alt="433122791-4a2d9ffc-9326-45a3-9af1-d8182eb970eb" src="https://github.com/user-attachments/assets/328addc4-e337-433b-ad2c-6ecdb4334a96" />


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
<img width="451" height="285" alt="433125770-498fc764-8666-4560-abbd-dc464b9246cc" src="https://github.com/user-attachments/assets/7dd4a22d-f35e-4309-8f58-9e771d9c919d" />



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
<img width="525" height="103" alt="433123111-0163c45c-d118-4b95-8276-b9ea3821ac0d" src="https://github.com/user-attachments/assets/477234b9-3d39-48e8-b4b8-22c0cfa3063b" />

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
<img width="512" height="334" alt="433126073-274f4167-a4c1-490a-bfa9-8972fa71ba0a" src="https://github.com/user-attachments/assets/fdc34e50-7e6b-44c6-84ad-e0171d3fe7aa" />

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
<img width="516" height="367" alt="433126113-496ecbc9-ed58-483e-b5bf-29c0b7621cda" src="https://github.com/user-attachments/assets/7dcc1b58-b41f-4c0b-9229-8669b6b2bc39" />

 
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
<img width="450" height="248" alt="433126340-634b332f-c989-46e7-b56e-de016a57b0f4" src="https://github.com/user-attachments/assets/358a243a-5eb3-4183-b451-9c79d4dbac9c" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="512" height="249" alt="433126373-f30e90b4-09f5-4eec-849b-b2a195f743d5" src="https://github.com/user-attachments/assets/d2d612f5-7622-452b-9a0c-044623463cc2" />



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
<img width="390" height="78" alt="433126399-050c4b24-a847-43ee-9a48-b1264d2540ad" src="https://github.com/user-attachments/assets/83d6def0-30d0-41f9-ad7b-7ce566c48d1e" />

 ./funcex.sh 
<img width="374" height="83" alt="433126422-839a71b9-e527-41c4-bb6d-4c841a8dcb2d" src="https://github.com/user-attachments/assets/c5ee3c3c-e8eb-473e-ae37-95f8c6e55a34" />

 
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
<img width="519" height="67" alt="433126451-73dc91e7-b52e-426e-9c4d-feadc6cb4644" src="https://github.com/user-attachments/assets/0f6dba63-0975-457b-a292-cc5cb8eb94f7" />

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
<img width="491" height="57" alt="433128008-1163e4c4-4e35-4d86-9e94-3a27033e52fe" src="https://github.com/user-attachments/assets/b557ae46-c4d0-4225-9081-acd166c78ed1" />

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
<img width="493" height="53" alt="433128526-8a0dab6c-d1fa-4189-a650-6e5d1e5f8d83" src="https://github.com/user-attachments/assets/631eaf0e-4741-4aa5-928b-48e40b2ea5da" />

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
<img width="320" height="372" alt="433128558-c9006d8d-2ded-45a1-bb0a-7320756db0c4" src="https://github.com/user-attachments/assets/eb1686bc-b959-4c11-8da2-7284a0199fe5" />
 
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
<img width="406" height="552" alt="433128593-49e26e36-e08c-438e-b947-c810d87fd39a" src="https://github.com/user-attachments/assets/678e5325-cdc1-4713-a9dc-675a7b6a611f" />


# RESULT:
The Commands are executed successfully.
