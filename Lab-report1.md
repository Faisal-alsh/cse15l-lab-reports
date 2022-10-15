### Lab Report 1



## Faisal Alshinaifi 


  - [Installing VScode](#installing-vscode)
  - [Remotely Connecting](#remotely-connecting)
  - [Trying Some Commands](#trying-some-commands)
  - [Moving Files with `scp`](#moving-files-with-scp)
  - [Setting an SSH Key](#setting-an-ssh-key)
  - [Optimizing Remote Running](#optimizing-remote-running)



## Installing IDE:

To install VScode, start by visiting [https://code.visualstudio.com/download](https://code.visualstudio.com/download), then download the appropriate version. When you open the app, you should see something similar to this.

## Remotely Connecting:

Open the terminal in VScode.
<img width="1470" alt="VsOpen" src="https://user-images.githubusercontent.com/51794365/195963367-c8d1586a-1895-406e-a537-4cd65accdcd3.png">

Then, type `$ ssh cs15lfa22zz@ieng6.ucsd.edu.` and replace **cs15lwi22zz@ieng6.ucsd.edu.** with your own address

You might see this massage if this was your frist time to connect: 

**⤇ ssh cs15lfa22zz@ieng6.ucsd.edu**
**The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.**
**RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.**
**Are you sure you want to continue connecting (yes/no/[fingerprint])?**

**Enter yes**

Then Enter Your password

Then Somthing like this should show up: 


<img width="570" alt="Part2CSE15L" src="https://user-images.githubusercontent.com/51794365/195963748-96c59d80-5b4f-40ae-afd6-01fafa4a3381.png">

**NOW TRY SOME COMMANDS!!**

<img width="771" alt="Screen Shot 2022-10-14 at 6 48 00 PM" src="https://user-images.githubusercontent.com/51794365/195963817-3d0d4547-2514-4738-bbdd-a5863e6650bc.png">
 Cd.. lets you gp back a derictory
 
 ls   Gives you the conteants if the given directory
 
 Cat Gives you the code of the code file 
 
 Javac Compiles the java file
 
 


## NOW We move Files with `scp`:

<img width="771" alt="Screen Shot 2022-10-14 at 6 48 00 PM" src="https://user-images.githubusercontent.com/51794365/195964037-7c2b7b4d-a698-4b17-8b69-2eba7aeb6a27.png">

Use `scp` command to copy files from the client(your desktop, to the server).

## Let's set up an SSH Key:

This step will help you avoid typing down the passowrd when running ```ssh `or` scp```.
Start by running `ssh-keygen` on your device, which will creates two files *public key*(`id_rsa.pub`) and *privte key*(`id_rsa`) stored in `.ssh`. 

<img width="1470" alt="Part7CSE15L" src="https://user-images.githubusercontent.com/51794365/195964252-ba2af35f-351c-42a0-9f67-ccc0b2ccf4f8.png">

## Optimizing:

To make running commands on the server a bit easier and faster you can do the following:

```
 ssh cs15lfa22ta1@ieng6.ucsd.edu "javac WhereAmI.java; java WhereAmI"
```
<img width="566" alt="Part8" src="https://user-images.githubusercontent.com/51794365/195964781-f4aeb83f-cf69-4ecf-9503-d21794fbe6a8.png">
