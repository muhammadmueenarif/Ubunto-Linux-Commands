https://www.jslinux.org/ to run Linux commands live.

1. Change Directory 
cd command You can browse the file system with the command line.
pwd command to see the current folder 
cd Desktop to change your folder to Desktop type
cd.. To move up a folder type
cd~ To move to your home folder type



2. Show file content 
Echo 
echo command is one of the most basic commands. as the name is implies, it just echoes your data.  
echo "Heloo how are you", this will output same on screen. anything between the quotes will be echoed on screen.

you can echo any type of text and save that immediately into a file by typing the > symbol. 
e.g., echo "I am fine" > newfile.txt.  So it created a new file with text that we write (I am fine). 
So if you open file txt so you'll see it contains the same text.

if we run it again (echo "I am fine"), it doesn't contain an extra line, it just overwrites it. (only single line will be showing. 
it does not duplicate). 
if we change the text (echo "how was your day today ") and we open file again, you'll see it 
overwrite previous line of I am fine or whatever written. the text which we wrote before is now replaced.

So if you want to append, add to end of the file, type >> symbols. Echo “i am fine” >> example.txt
if we run several. now it will duplicate. instead of one,it writes as many times we press enter. 
if we again write echo "how are you" > example.txt then it will overwrite all the file and only this line 
will be showing in file. it overwrites the file completely All the contents is gone.



3. ls command 
it lists the directory contents of current directory. to use LS commands just type LS and press enter and
it will list the directories, files and folders.
LS commands lists the same files and folders, it does that in text format so you don't have any icons.

So by default, the ls command or the file explorer doesn't show hidden files. To show all the files inside the folder you can 
type LS -a and that lists all the files, including hidden files. or in your file explorer click show hidden files.
And then you'll see hidden directories.

there's many parameters we can do with ls command. For example, can do a long list of files or long formats 
when we type ls -l.
So that tells you more information about the thousand folders. Like, when is it lost? Who is the owner of the file? 
The group. That is what's group is it part of and the file folders permissions.
So the ls -l, you can get some more information like the date modified and so on. You can also show the file 
sizes in human readable formats.

So when we type LS minus H. You won't see any actually anything. So what you can do is ls -h -l,
But we can type the commands, ls -h  and that tells you the size of the files as well. (ls -hs also used)
So it tells that in human-readable, readable format like kilobytes, megabytes and so on, gigabytes.

we can type man ls and It will list all the flex that we can use with ls command.
With the ls commands you can change the default behavior. For example, the -h command, must be used with -s 
flag to print sizes.
And you can find all of the flags inside this.  to exit this page, press Q. So to open it man ls, then you 
can read the menu page with all the parameters that can be used for the LS commands and press Q to quit.

Now another way to do it is ll that list does the same as ls -l. So now you see the dates and also the username and group. 
So ll, and ls -l will do the exact same thing.
like ls -H -S for the human readable formats, but maybe we want the long format. so ls -h -s -l
So this is one way to write it, but you can also combine those. So you can say ls  -hsl. it does the same 
thing as typing that separately (ls -h -s -l).



4. Show file contents
cat command
it is used to get contents. it outputs the file contents. For example, we have two files and we could Type 
cat filename and it shows the contents of file. If we open the same file with a text editor, you'll see 
it's exactly the same file contents.

Sometimes the cat command is not available. then we can use alternatives like see cat spelled 
backwards tac and it does exactly the same thing.
However, the tac command has less funcnality. So if we type cat --help, we see there are some flex that can be used. 
tac doesn't have that many functions.

Another commands you can use is the head commands. for example head example.txt you'll see it outputs the same thing. 
it's an alternative. 
difference with the head commands is that shows from the top the first lines where you can specify. for example 
if we write head -n 1 example.txt ,now only the first line from the top of file will be shown. and 
similarly we can specify up to as many lines as we want

So another one you can also read from the bottom using the tail command. If you say tail example.txt, it just 
shows the file and the first line from the bottom or the second line. example tail -n 1 example.txt, So tail 
commands can be used to output as well.

There are some alternative to cat commands like xxd commands. So when we type xxd with any NFL, we can see 
file content. However, this is in hexadecimal format.  it's a computer format.
And another trick that can be used is using base 64.  example base64 example.txt | base64 --decode. 
it also shows the file contents. in case Cat Command is not available. in 99% of the cases, cat commands available. 



5. Find 
with find command we can easily find files or files of a certain type.
For example, we can find files in the default directory. if we want .txt files. we write find -name *.txt.
We edit between quotes and you'll see it finds the .txt files in the Home Directory. find -name "*.txt".

pwd is used to check current working directory. there are other files and if hidden files, then they will be shown also. 
to check manually, go to show hidden files option in the directory and check.
we can easily find files on system of a certain type. we could find dot text or any format.
For example, if you are searching for word documents, you could say type doc or doc X. find -name *.docx.
Maybe you search for mp3 files and you will type mp3.

if we want to find file of certain name. So maybe file that contains word Linux. then we will type * on 
both sides of name. this will search for any file on home directory, which the name is inside or with word Linux inside. 
find -name "*linux *" it finds files with the word Linux inside it.

So let's search for files with the words example we would type find -name "*example *". 

So if we create a new file. And we save it as the_example.txt. And now if we search for example again by 
command find -name "*example *". it will show all files with word containing example in it (not necessary 
files that only start with example).

if we write command without *, it will show only files that start with word example.
So when you put the asterisks in front, then the file name can contain that word.
It can be ending with any other file formats. So if you only want to txt you would type Ending with .txt, then it will give only ending with .txt. (find -name "*example.txt")
So if you just want it containing the words, write * on both sides.


6. Grep 
we can search within text files or within files using the grep commands. grep commands can search within a 
specific file. For example, we have file txt and we could search for the word x inside file txt and that will 
show you all the lines with the word text. (grep "text" example.txt). So it will show the lines containing words text.
with grep commands, we can search within files and it doesn't have to be just a single file. we can search 
in a bunch of files. For example, we can search for word file in any text file. So grep "text" *.txt that 
would search for the word file in any of the text files.

And it will show all text files on system that contain the word file. Or we might search for word Linux 
inside text files.
it can be case sensitive, if we do a capital L, we'll see it finds another file. So the grep commands and 
things in general in Linux are case sensitive.
it matters to use capital letter or lowercase letter which grep commands can search within text files or 
within any type of file. for example, search for the word linux in any of the files on the system. 
grep "linux" *.
So if you do asterisks you can find it searches any file in your home directory.
If you just want to see only txt file, you can type *.txt. So you'll see it found one file containing that word.


7. Sudo 
Linux is a multi user system, there can be one or more users on the system.
run the command whoami to see current user.

there's always one user on Linux system which is administrator. administrator is called root. Root has its 
own file directory which is in the directory/ root.
So if you find it in the folder and location, you'll see there is a root directory that you cannot enter. This is permission denied. So that's root and only admin can access. There actually contains the files and folders of the user roots.
Root is the system administrator.
even though I am not root, I might be able to run commands as root. with sudo commands we can execute commands 
as if you are root (administrator).
if we type sudo space and then any command for example who am i we'll see now it outputs root. it executes 
commands after sudo as root.
when we type sudo it will ask password of root user. But it doesn't have to always be the case.
if I were to enter or list of files in the root directory. So ls /root. It says permission denied. However
if we do the same thing with pseudo inference, it will try that commands as the root user.
we will see it now executes that command without problem.
when we run sudo command or any commands as root user, as administrator. we get permission denied or get 
password prompt. we need a root password to actually run the commands.
if it does not ask for password, then it is a security problem because any user on the system will run commands 
as the administrator without typing the password.


8. Chmod
each file in Linux has permissions. we have some files on the system. We could right click on the file,
click properties and click tab Permissions. inside permissions, we have several things. So default user can 
read and write files. Users, members of the group linux can only read files and others can only read file. 
there's also a permission to allow to run this file as a program. different permissions can be set.
when we type before ls -l, we saw permissions of files here on the left (r for read and w for write. 
r for read write, x for execute file as program). for example, we check file example.txt so I right clicked 
on example txt with properties and have permissions. So if I do ls -l  So example txt you'll see the permissions 
so there is read right for the user.

rw-r-r kali (the user kali can read write and user kali can read).
So if we put everything to read write, then anybody on the system can read and write this file. 
right click on the file and click on permission, If we list it, you'll see three boxes permission because 
first is permission for owner reads write, then for the group reads write and then for others reads write.
Seeing the multiple mods. (when you type command ls -l example.txt, the results showing first permission 
for the user or owner, second permission will be for group and third will be for others).

We can also set permission with cmd instead of doing this with a graphical user interface. We can type 
chmod +x example.txt. it changed the permission to executable with x word. the file is executable for anyone.
to remove that permission, we can type -X.
So for example, you might say user should be able to read write. The group should be able to read. 
And others should be able to read. 
(chmod U=rw, g=r, o=r example.txt). we can change permission by writing (r, w).



9. Wget 
You can download any file from the internet inside your terminal. wget https://website.com/file.zip (file 
name with extension).
So depending on the file size, it can take shorter or longer time.  So now I have that file downloaded 
onto the computer.
one thing you noticed is that it shows all of that output into the terminal. while it's downloading, we 
can't do anything else. So we can download in the background. if we type - b before URL (wget -b URL), 
then download in background. see now we don't see any outputs. We can continue using terminal while download.


10. Curl 
curl commands can be used to interact with the internet. you can use the commands with several protocols.
Protocol is the way that data is used online, like HTTP protocol which is used in the web.
there's many other protocols. FTP for file transfer and Which for communicating or remotely controlling a computer.
curl works with all of communication protocols, for example, interact with the HTTP protocol. if we type 
curl -- help, we see all of the things it can do.

We can use curl with some website, like curl HTTP://www.youtube.com. it use web protocol to get data from 
server, from this computer.
if type curl, we'll see that it gets data and download the data from that computer.
we can limit the speed. For example, curl protocol with URL --limit -rate 1234B.

You can also save the output. So you can say -o with some file name. So for example, curl URL -o computer.html.
So that's downloaded the contents into a file called computer.html.
If we type curl with any website like google.com, it gets the contents of that computer into our computer 
and we can view this contents in termnal.



11. Archives 
sometimes we find archive files that can be a zip file or .tar.gz file. Or it can be seven zip file. we can 
extract files using GUI in the folder we want. 

we can extract in terminal.  we type 7 zip x filname.extension(pictures.7z). make sure that the file format 
is correct with the command that we type.  Press enter and it extracted those files inside the same directory.

if we have a zip file, type unzip pictures.zip and you'll see it extracted the files in that archive. any 
archive file can be extracted using terminal.

it could be a zip file or a seven zip file, many others as well. it can be tar.gz.
if we have a dot set file, to extract it we can type tar -xf pictures.tar.gz. it will extract Archive files. 
So similarly many types of archives are possible, but the principle is the same.

we cancreate our own archive in terminal. we can Right clicked, select it. clicked archive and then did it in the graphical interface.
we can archive in terminal. Go to directory. cd directory name. we type zip filename(pictures.zip) and then 
write names and extensions of all files you want to add. 

we can zip all the files of folder by zip pictures.zip *. So it will create archive using the terminal.
If we want to create tar.gz file, type tar -czvf pictures.tar.gz *. all your files will be zipped. 


12. Clear 
to clear the terminal. We can also use the ctrl+l command. It does not really clear because when we scroll 
top, we can see previous commands there on screen, 

Ctrl + U to clear everything from left of the cursor. 

Ctrl +K to clear everything from right side of cursor. 
Reset command. 


13. Whatis 
it give us one line description of the command. Like whatis reset will tell about reset command, 
Whatis history. 

Help cd. Will give us all details about cd commands. 
Man cd will give detailed info about cd command. Man pwd will give about pwd command and so on. 

If we forget command and write hi and press tab button 2 times then it will show commands starting with hi. history
Apropos his, this will show all similar commands with his. 


14. History 
it will show recently used commands. History 5, will show last 5 commands. We can use !4 to run 4 number 
command from history. 
If we want to search within history of command, we can use ctrl + r. And type command. 
We can clean command history by typing history ~c. 


We can scan our linux system using terminal for viruses. we need to install clamav software for this. free. 
sudo apt-get install clamav. 
clamscan -r foldername. this will scan our folder like clamscan -r /home/pictures. once scan is completed we 
can see summary. hidden files are also scanned. 


15. Network Scan 
nmpa localhost. this command will show open ports. if does not show then we need to install this command first 
with package manager. in setting > sharing section, we can turn on sharing. nmap is used by system administrator, 
Network manager, and also hackers. hackers can get your ip address and check which port is open. in setting, 
sharing, Network, and setting option you can check your ip address. 
nmap ipaddress. it will show open ports. 