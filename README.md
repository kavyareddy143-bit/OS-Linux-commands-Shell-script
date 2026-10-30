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

<img width="377" height="251" alt="image" src="https://github.com/user-attachments/assets/4f7995d0-0236-481f-9dbb-3437d7c5c771" />

cat < file2
## OUTPUT

<img width="382" height="251" alt="image" src="https://github.com/user-attachments/assets/8d889d52-22e6-4d84-a191-b53dea03369b" />

# Comparing Files
cmp file1 file2
## OUTPUT
 
 <img width="565" height="107" alt="image" src="https://github.com/user-attachments/assets/d8eaaabe-99d5-480a-9894-b4c2c55c0547" />
comm file1 file2
 ## OUTPUT

 
 <img width="506" height="412" alt="image" src="https://github.com/user-attachments/assets/9fd27278-a745-420f-8836-2265ea9adaad" />
diff file1 file2
## OUTPUT

<img width="495" height="481" alt="image" src="https://github.com/user-attachments/assets/fdb285e9-fbf9-48c7-bab7-1cee76db87f4" />
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

<img width="492" height="222" alt="image" src="https://github.com/user-attachments/assets/bf925f13-6298-4952-96e2-a570bbf346fb" />


cut -d "|" -f 1 file22
## OUTPUT



<img width="585" height="212" alt="image" src="https://github.com/user-attachments/assets/273f64d5-dad8-4159-879d-ec8379b36535" />
cut -d "|" -f 2 file22
## OUTPUT

<img width="588" height="215" alt="image" src="https://github.com/user-attachments/assets/65e411ae-3f15-4a33-ba16-df7b030c6f71" />
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

<img width="526" height="123" alt="image" src="https://github.com/user-attachments/assets/325914f5-aa3b-4168-8f9e-9b9a2bd0340f" />


grep hello newfile 
## OUTPUT

<img width="518" height="106" alt="image" src="https://github.com/user-attachments/assets/508f9331-dccf-4b14-95ab-de0b66428165" />



grep -v hello newfile 
## OUTPUT

<img width="568" height="152" alt="image" src="https://github.com/user-attachments/assets/d2c9d924-8e78-4f41-9701-a956dbdc634f" />

cat newfile | grep -i "hello"
## OUTPUT
<img width="683" height="135" alt="image" src="https://github.com/user-attachments/assets/f417b539-1ad3-475e-bad9-b1e96fc40d9d" />
cat newfile | grep -i -c "hello"
## OUTPUT


<img width="670" height="100" alt="image" src="https://github.com/user-attachments/assets/73b80652-e0db-4ec8-b0bb-eca51c180924" />


grep -w -n world newfile   
## OUTPUT


<img width="622" height="147" alt="image" src="https://github.com/user-attachments/assets/924057e5-511e-4501-aacf-ba283e08f62d" />
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

<img width="688" height="142" alt="image" src="https://github.com/user-attachments/assets/e4e04581-bb17-4832-bc35-04cffb40c217" />


egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="681" height="131" alt="image" src="https://github.com/user-attachments/assets/1ddcfcd2-597e-46cb-9973-84250b94e47f" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="663" height="126" alt="image" src="https://github.com/user-attachments/assets/73f63460-05eb-4e20-a5fe-17b4f647b64c" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="631" height="115" alt="image" src="https://github.com/user-attachments/assets/cdaebbfa-481f-4176-bfab-68d01824a044" />

egrep '(world$)' newfile 
## OUTPUT

<img width="623" height="135" alt="image" src="https://github.com/user-attachments/assets/2de0686e-1975-4d1b-961e-73d8f61a0d85" />


egrep '(World$)' newfile 
## OUTPUT

<img width="606" height="102" alt="image" src="https://github.com/user-attachments/assets/54013039-1c4f-406f-ae19-2a68c21ca24d" />

egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="697" height="180" alt="image" src="https://github.com/user-attachments/assets/a298e576-d9bb-42d8-b599-0d0414d5aa82" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="558" height="100" alt="image" src="https://github.com/user-attachments/assets/42130578-809b-4003-b9e5-99fa21696c0e" />
egrep 'Linux.*world' newfile 
## OUTPUT


<img width="677" height="107" alt="image" src="https://github.com/user-attachments/assets/0df2a8a7-8d9a-4221-951b-af5f1eab9e25" />
egrep 'Linux.*World' newfile 
## OUTPUT

<img width="670" height="107" alt="image" src="https://github.com/user-attachments/assets/53c825b1-ba35-4940-a6ec-f0afb9d2919b" />

egrep l{2} newfile
## OUTPUT


<img width="537" height="147" alt="image" src="https://github.com/user-attachments/assets/128b1a21-e950-4b3d-9ff7-14b134aac379" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="596" height="177" alt="image" src="https://github.com/user-attachments/assets/3df60db9-d25e-481b-b5b2-754991535a75" />


# RESULT:
The Commands are executed successfully.
