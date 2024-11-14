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


