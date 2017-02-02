# Commands


## PI 102: Introduction to Command Line
## FUBAR Labs 
## Topics

* [Basic UNIX Commands](#basic-unix-commands)
* [UNIX Shell Environment and Commands ](#update-upgrade)
* [Update and Upgrade Your System]
* [Software Installation  ]
* [Command Line Remote Access] 
* [System Commands ]
* [Network Commands ]
* [File Directory Commands ]
* [Reboot and Shutdown ]

### [Basic UNIX Commands](#basic-unix-commands)

| Command        | Description           |
| ------------- |:-------------:| 
|`ls` 			|	list directory contents|
|`pwd`			|	print working directory	|	
|`cd`			|	change current directory|
|`mkdir directory`|	make directory|
|`rmdir directory`|	remove directory|
|`rm -rf`		|	recursively removes directory|
|`echo`			|	display arguments to screen|
|`man`			|	display online manual|
|`exit`			|	exit shell|
|`clear`		|	clear screen|


### [Update and Upgrade Your System](#update-upgrade)

`apt-get update` 				Update Packages from a Repository		
`apt-get upgrade`				Upgrades Packages Already Installed with Newer Version

`apt-get update && sudo apt-get upgrade`

### Software Installation/Uninstall (Packages, Repositories, Dependencies)
`apt-get install package_name`	Install software/package from a repository

`apt-cache search search_string`	Find package in a repository

`apt-get remove package_name`	Uninstall package

`dpkg --list`				List installed packages

`dpkg --status package_name`		Display information about an installed package		
						
### Finding and Sorting things

`grep -r "username" .`			Find a word used in files from the current directory down

`ls | sort`					List all current directory files and sort in numeric alpha order

`find . -name "robots.txt"`		Find a file and print it’s name

### Breaking down the command line

.			the current directory
..			the directory above
/			the root of the file system
&&			combine two commands
\			let one command take several lines
|			pipe output of one command into the next
>			send to a file and erase contents
>>			send to a file and append contents

### What’s in a file?
cat filename

### How much space is left?
df -h

What is /dev?

What is /etc?


### System Permissions
Permission Type 
```
r  			read
w 			write
x 			execute
```

Permission Categories
```
u			user
g			group
o			other
a			all
```

### File Permissions
```
Change file permissions

chmod  					change mode command
+ - =						add, subtract or set permissions

Change file ownership
chown	 [owner][:[group]] file	change the owner and group owner of file or directory
```

### Create your own command alias

### How to use tar
```
tar mode[options] pathname		
tar modes
c		Create an archive from a list of files and/or directories
x 		Extract an archive
r		Append specified pathnames to the end of an archive
t  		List the contents of an archive
```

htop vs top

How to kill a process

tmux for multiple consoles

Use screen to talk to a serial port 

Change your password with passwd

Interact with your network device
```
ifconfig
```

What’s your machines kernel version and details?
```
uname -a
```

What command am I really using?
```
which ls
```

less is more
```
man less	manual page for less
cat		display the contents of a file
more		page through the contents of a file
less		scroll up and down and search a file
```

What’s at the end of a file? Monitor new entries in a file.
```
tail system.log
tail -f system.log

Terrible superpowers don’t do this:
sudo su -l 
sudo su -l yourfriendsaccount
```

Getting stuff from the internet with curl or wget



Vim survival guide
```
vi file			Invoke vi on file
view file			Invoke vi on file in read-only mode
vi -r file			Recover file and recent edits after a crash
ctrl+F/ctrl+B		Scroll forward/backward one screen
ctrl+D/ctrl+U 		Scroll down, up half-screen
ctrl+E/ctrl+Y		Show one more line at bottom/top of window
h j k l			Left, down, up, right by character
w W b B			Forward, backward by word
e E				End of Word
i / a 			Insert text before/after cursor
I / A				Insert text before beginning/ after end of line
o / O 			Open new line for text below / above cursor
cw 				Change word
cc  				Change current line
C				Change to end of line
r				Replace single character
R				Type over characters
x				Delete character under cursor					
X				Delete character before cursor
dw 				Delete word
dd 				Delete current line
D				Delete to end of line
p P				Put deleted text after/before cursor
:w				Save file
:wq				Save file, quit file
:x				Save file, quit file
:q 				Quit file
```
You hate vim now what?
* pico
* nano

### How to use tar
```
tar mode[options] pathname		
tar modes
c		Create an archive from a list of files and/or directories
x 		Extract an archive
r		Append specified pathnames to the end of an archive
t  		List the contents of an archive
```
tar xvzf extract.tar.gz
tar cvzf backup.tar.gz ./mydir


