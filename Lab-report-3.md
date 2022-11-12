### Lab Report 3
# Researching Commands


-

---

## ```Consider the command find```

When running the command 'man find' I can find (Pun not intended) the commands it can uses and there descriptions.

<img width="1470" alt="Screen Shot 2022-10-31 at 1 48 18 AM" src="https://user-images.githubusercontent.com/51794365/198968503-1b148a49-26e4-4792-9d6c-c5d868874c79.png">
 
 
 ## ```- name```
 To illustrate the use of the find command I used it with -name and '*'. the '*' is as if saying give me what ever thing that fit the format of *.java so like anything.java, and the for the -name as described in the manual :
 
 
       -name  This option is supported, but POSIX conformance depends  on
              the  POSIX  conformance  of the system's fnmatch(3) library
              function.   As  of  findutils-4.2.2,  shell  metacharacters
              (`*',  `?'  or  `[]' for example) will match a leading `.',
              because IEEE PASC interpretation 126 requires  this.   This
              is a change from previous versions of findutils.
              
             
<img width="1470" alt="Screen Shot 2022-11-11 at 8 17 46 PM" src="https://user-images.githubusercontent.com/51794365/201456689-6459a33a-0c19-4705-a111-a33df63c130b.png">


You can  use "*" The star charectar to genrilize the search. For example In the screenshot below I have Search for anything that Starts with "chapters" it does not matter what comes after, this is the power of the Star charecter with the - name command.

<img width="1470" alt="Screen Shot 2022-11-11 at 8 18 33 PM" src="https://user-images.githubusercontent.com/51794365/201456700-6e2c7961-fd11-4302-80e4-25eb06fe8856.png">

Now I have Searched for anything that Starts with a "s"

<img width="1470" alt="Screen Shot 2022-11-11 at 8 19 32 PM" src="https://user-images.githubusercontent.com/51794365/201456739-80cf6d72-b498-4a1c-9af0-71a8a56a3168.png">


 ## ```- type```
 
  To further illustrate the use of the find command I used it with - type , This command is a usful quiry to add to the find fuction to specify the type of the intended result. It can be used to specify multiple types like : 
    File is of type c:

              b      block (buffered) special

              c      character (unbuffered) special

              d      directory

              p      named pipe (FIFO)

              f      regular file

              l      symbolic  link;  this is never true if the -L option
                     or the -follow option is in effect, unless the  sym‐
                     bolic  link  is  broken.   If you want to search for
                     symbolic links when -L is in effect, use -xtype.

              s      socket

              D      door (Solaris)
              

These are all the Directories in ./technical
<img width="1470" alt="Screen Shot 2022-11-11 at 8 20 47 PM" src="https://user-images.githubusercontent.com/51794365/201456774-a77bb0b1-5979-4559-a596-50511a17bcc9.png">

These are all the Files in ./technical

<img width="1470" alt="Screen Shot 2022-11-11 at 8 21 42 PM" src="https://user-images.githubusercontent.com/51794365/201456804-fed9e7a8-b167-4cea-9d40-37e31abc5893.png">

Result of the command:

<img width="1470" alt="Screen Shot 2022-11-11 at 8 21 59 PM" src="https://user-images.githubusercontent.com/51794365/201456810-eef6fcdd-0304-4d03-89b0-45e835504c73.png">


These types are not in the ./technical folder

<img width="1470" alt="Screen Shot 2022-11-11 at 8 23 05 PM" src="https://user-images.githubusercontent.com/51794365/201456837-41245735-d0bf-4c59-9c4c-000b1e4a1f4d.png">





