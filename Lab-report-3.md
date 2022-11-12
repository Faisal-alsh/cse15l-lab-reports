### Lab Report 3

Faisal Alshinaifi

# Researching Commands

---

## ```Consider the command find```

When running the command 'man find' I can find (Pun not intended or maybe it is...) the commands it can uses and there descriptions.

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


 ## ```- size```


Lastly, to illustrate the use of the find command I used it with - size, This extra piece of Query can be used in data mangement, if a developer wants to know what files are taking space or what is the number of large files he can utilize - size . The decreption from the manual:

       -size n[cwbkMG]
              File  uses  n  units  of space, rounding up.  The following
              suffixes can be used:

              `b'    for 512-byte blocks (this is the default if no  suf‐
                     fix is used)

              `c'    for bytes

              `w'    for two-byte words

              `k'    for kibibytes (KiB, units of 1024 bytes)

              `M'    for  mebibytes  (MiB, units of 1024 * 1024 = 1048576
                     bytes)

              `G'    for gibibytes (GiB, units of 1024 * 1024  *  1024  =
                     1073741824 bytes)

              The  size  is  simply the st_size member of the struct stat
              populated by the lstat (or stat) system call, rounded up as
              shown  above.   In  other  words,  it's consistent with the
              result you get for ls -l.  Bear in mind that the  `%k'  and
              `%b'  format specifiers of -printf handle sparse files dif‐
              ferently.  The `b' suffix always  denotes  512-byte  blocks
              and  never  1024-byte blocks, which is different to the be‐
              haviour of -ls.

              The + and - prefixes signify greater than and less than, as
              usual; i.e., an exact size of n units does not match.  Bear
              in mind that the size is  rounded  up  to  the  next  unit.
              Therefore  -size  -1M is not equivalent to -size -1048576c.
              The former only matches empty  files,  the  latter  matches
              files from 0 to 1,048,575 bytes.


Examples:

Number of Files that are larger than 100 kibibytes :
<img width="1470" alt="Screen Shot 2022-11-11 at 8 32 08 PM" src="https://user-images.githubusercontent.com/51794365/201457157-a4f019b9-f35e-4070-a26d-af429a11ff90.png">

Number of Files that are smaller than one kibibytes!
<img width="1470" alt="Screen Shot 2022-11-11 at 8 33 42 PM" src="https://user-images.githubusercontent.com/51794365/201457200-dfc3ae2a-72c3-44e8-91d7-b31e6861d5f4.png">


THANK YOU!!

Number of Files that are smaller than one byte : (SPOILER ALERT!: its zero):

<img width="1470" alt="Screen Shot 2022-11-11 at 8 35 22 PM" src="https://user-images.githubusercontent.com/51794365/201457244-8e22252e-9f44-46dc-abaa-139651136bb2.png">
