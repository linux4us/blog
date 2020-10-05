Ranger, the best file manager for Linux



I've been using the Ranger file manager on Linux for quite some time. It's one of my essential tools in the terminal and together with i3 and Vim, Vimium and the shell itself, makes my life so much easier. On this post we'll see why use the Ranger file manager, learn some tips and 


Why Ranger
But, with some many file managers out there, why Ranger. Here's my reasons for it:
A terminal-based file manager: I spend most of my time on the terminal, this is where I'm most productive. Ranger 
Vim-based shortcuts: this is probably one of the biggest strenghts in my opinion. Vim shortcuts are intuitive (once you know them) and really, really productive.
Lightweight: despite being written in Python, ranger is fast enough for most systems
SSH-ready: because it runs on the terminal, it's available for me remotely via SSH. This is a major plus
Bulk-operations: ranger makes running bulk operations really simple and saves-me a lot of time
Text-editor integration: with its text editor integration (Vim on my case), I can do crazy stuff from Vim to manage my files (we'll see later)
Git integration: ranger can also integrate with git making your life even easier.

TIP: Looking for an even lighter filemanager, check nnn.


Installing Ranger
At this point, Most distros sould have Ranger packed up in their repositories. 

Installing on Ubuntu/Mint/PopOS/Elementary, etc.
On Ubuntu-based distros, installing ranger should be as simple as:
sudo apt update && sudo apt install ranger -y

Installing on Fedora/CentOS/RHEL:
On RH-based distros, installing ranger would be:
sudo dnf update && sudo dnf install ranger -y


Getting to know Ranger
Start ranger by typing ranger on the terminal. This is what you should see initially. The default view consists of 3 panes. In the middle you'll see the files in the current folder. On the left, the previous folder and on the right a preview of the current file. Most of the descriptions are already available on the image, feel free to compare it to your system.




Navigating the files
The first essential thing to know is how to navigate your files. You can use your arrow keys or, more preferedly, use the hjkl.

TIP: hjkl is the default navigation in Vim which Ranger, a Vim-inspired file manager follows. It may feel uncomfortable at the beginning but soon you'll realizing that keeping your fingers on the home row will allow you to type faster, be more precise and save some muscle movements.

As with Vim, you'll navigate with hjkl. Once you get used, this is very productive as your hands will be kept on the home row (where they should be):
h: to the upper folder
j: go up in the current list
k: go down in the current list
l: go to the inner folder
]: move to the upper parent folder
[: move to the lower parent folder
gg: goes to the top of the list
G: goes to the bottom of the list
gX: options to go (g) to specific folders. Ex: gh (go home), go (/opt), gm (/media), etc

We can also combine motions and keywords (like in Vim) to jump further. For example:
3j: would jump 3 files on the list
4[: to move up 4 times the parent folder


Getting Help
Before learning the essential commands, let's learn how to get some help. Typing ? will show you this bar at the bottom:


From here, type:
m: to access the man page. There's a lot of important information there
k: to learn more about the current keybindings
c: to learn about the commands
s: to view/edit your settings

Accessing the man(ual) page
As stated previously, typing ?m the main screen will show you Ranger's manual. There's a lot of info here. Feel free to explore.
TODO::ADD-IMG

TIP: The manual is opened by default with less that also uses keybindings. You can use your arrows or jk to move up/down. You can also use / to search, d/u for page up, page down, and q to quit etc.

Current Keybindings
Typing ?c takes you to the current keybindings. You'll see a screen like the below where you'll learn a lot. Note: the same Vim keywords apply here. 

TODO::ADD-IMG


The command shell
If you press : you'll have access to a command shell where you can type commands. For example, you could type :mkdir <dirname> if it makes your workflow quicker. To view a list of all the commands supported on your system type ?c for help. You should see a screen similar to the above. Remember, Vim keywords to navigate and q to quit.
TODO::ADD-IMG


Settings
Typing ?s will show you your current settings. There's a lot to customize there. Feel free to explore.


Essential Commands
Let's now review some essential commands.

Navigating
As with Vim, you'll navigate with hjkl. Once you get used, this is very productive as your hands will be kept on the home row (where they should be):
h: to the upper folder
j: go up in the current list
k: go down in the current list
l: go to the inner folder
]: move to the upper parent folder
[: move to the lower parent folder
gg: goes to the top of the list
G: goes to the bottom of the list
gX: options to go (g) to specific folders. Ex: gh (go home), go (/opt), gm (/media), etc
Ctrl+D or J / Ctrl+U or K: Move a half page down, up

We can also combine motions and keywords (like in Vim) to jump further. For example:
3j: would jump 3 files on the list

Copying and Pasting
Copying and pasting also follow Vim's nature where y (yank) copies and p pastes.
yy: copy
pp: paste

Typing just y will show you other options:



Deleting files
To delete, we'll 
dd: cut
dD: delete

Typing d also shows you other options:

Filtering
Typing f on the main screen allows us to enter part of the file we want to find. By typing chan, ranger auto-filters for me entries that have chan on it:




Tabs
The main keywords for tabs are:
Ctrl-n: new tab
Ctrl-w: close tab
Tab: next tab
Shift-Tab: previous tab
q: close tab
Alt-NUM: move to tab NUM


Sorting
Sorting is also very intuitive in Ranger. By default, sorting is activated with the o keyword as shown below.

So, typing oX where X is listed below would:
ob: sort by name
oB: sort by name reverse 
os: sort by size
oS: sort by size reverse
om: sort by time
oM: sort by time reverse
ot: sort by type
oT: sort by type reverse

Bookmarks
We can easily create bookmarks with `X and go to them with mX (where X = a letter). 

Other Important Keywords
zh or Ctrl-h: show hidden files
S: open a terminal from ranger. Exiting returns to it
l: typing l on a file, opens it with your text editor
i: view the current file in fullscreen
E: edit the file in your $EDITOR
W: opens Ranger's log
w: open the task windown (to view long operations, for example when you're copying big files)
/: search a file in the current folder
!: allows to quickly run a shell command

Bulk operations

Working with multiple files
Now that we know how to operate on single files, let's review some bulk operations. Ranger simplifies a lot working with multiple files. To select multiple files, press v (and uv to unselect all). You'll see that the selected files are highlighted in yellow:


You can unmark some files with space:


TIP: you can also use motions to mark/unmark certain files. For example, 4+space would select/unselect the current file + the next 3.


Next, proceed with copying (yy) or cutting (dd) and move it to the target destination with pp.









Default keybindings
The best way to learn the default keybindings is using Ranger's manual (man ranger). The most common keybindings are:
F1: open help
F2: rename a file
F7: create a folder
Ctrl-C: stop the current process
Ctrl-H: show/hide hidden files
Ctrl+D or J / Ctrl+U or K: Move a half page down, up
/: search a file in the current folder



Advanced Features


Configuration
You may get to a point where you'll be quite comfortable with the keybinds and the operations. The next thing to learn is how to configure Ranger to your needs. Essentially the configuration you'll have to modify will sit on ~/.config/ranger. Including:
Changing the colorscheme: with  `set colorscheme`
Sort options: 
Preview mode: 
Mouse integration: 
Aliases: 






Learning More
From here I'd recommend you exploring the settings, they keybinds and 

Conclusion


References
Ranger Official Repo | https://github.com/ranger/ranger
Ranger Official Site | https://ranger.github.io/
Ranger Wiki | https://github.com/ranger/ranger/wiki

See Also
