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
