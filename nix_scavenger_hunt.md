# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. /home/cabox/workspace

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?* LICENSE  README.md  challenge_files  nix_scavenger_hunt.m

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?* drwxrwxr-x  4 cabox cabox 4.0K Jun 27 14:35 .
drwxr-xr-x 11 cabox cabox 4.0K Jun 27 14:35 ..
drwxrwxr-x  8 cabox cabox 4.0K Jun 27 14:35 .git
-rw-rw-r--  1 cabox cabox 1.1K Jun 27 14:35 LICENSE
-rw-rw-r--  1 cabox cabox 1.4K Jun 27 14:35 README.md
drwxrwxr-x  7 cabox cabox 4.0K Jun 27 14:35 challenge_files
-rw-rw-r--  1 cabox cabox 5.5K Jun 27 14:38 nix_scavenger_hunt.md
-rw-rw-r--  1 cabox cabox  317 Jun 27 14:35 nix_scavenger_hunt_stretch.md

The results using the '-alh' option gives a much more detailed response than the ls command by itself. It outlines the permissions or each file, the owner, the group and if the document can be just read or if the user and write them. 

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/)Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*
'a' option= All. It ensures that it does not ignore entries starting with a particular value. 
'l' option= using a long listing format. 
'h' option= human readable. Prints sizes in human readable format. 

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?* bin boot dev etc fastboot home lib lib64 media mnt opt proc root run sbin srv sys tmp usr var

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:* /home/cabox

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:* /home/cabox



* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?* 3

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?* /home/cabox/workspace

* Press the up arrow on your keyboard. *What just happened?* pwd was automatically entered
* Press the up arrow a few more times. *What do you see?* various commands were scrolled through including ls and cd commands and their different variations. They are all commands that I have entered before.

* Run the `history` command. *What do you see?*
1  pwd
    2  1s
    3  ls
    4  ls -alh
    5  ls /
    6  cd
    7  cd /
    8  pwd
    9  cd
   10  pwd
   11  cd
   12  pwd
   13  cd ~
   14  pwd
   15  cd~
   16  pwd
   17  cd/root
   18  pwd
   19  cd ~
   20  pwd
   21  cd /root
   22  cd /home
   23  pwd
   24  ls /
   25  cd/
   26  cd/root
   27  cd challenge_files
   28  ls
   29  ls.demo
   30  ls .demo
   31  cd ..
   32  pwd
   33  history
It's a list of all the comands that I have been using

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?* cabox

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:* 
cabox    pts/0        Jun 29 21:06 (54.69.152.243)
cabox    pts/1        Jun 29 21:22 (54.69.152.243)
cabox    pts/2        Jun 29 21:22 (54.69.152.243)

* How long has your system been running? Use `uptime` to see, and *paste the result here:* 21:30:40 up 45 min,  3 users,  load average: 0.00, 0.00, 0.00

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?* This commands is showing all of the new processes that I have initiated durring this test run. It also shows the status of each process, when it was started, and which command initiated the new process. 

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?* two

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?* 01-15-2015 

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?* ./tmp/modi_laboriosam.txt

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?* two, Britt-Erdman.user and Lissie-Strosin.user

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.* serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo se
d corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt in
cidunt. Explicabo vel esse blanditiis dolorem culpa non quia.


### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?* it's a list of all of the file names in the challenge_files folder. 
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
The ls- alh | more command produces a much shorter list of results. It lists user files to D rather than to T, like the ls -alh command. Other than that, the data given in the other columns is identical.
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*       441  0.0  0.5  71260  2648 ?        Ss   20:45   0:00 /usr/sbin/apach
www-data   444  0.0  0.4 415720  2420 ?        Sl   20:45   0:02 /usr/sbin/apach
www-data   445  0.0  0.4 415720  2424 ?        Sl   20:45   0:02 /usr/sbin/apach
root       508  0.0  0.1  12740   848 tty1     Ss+  20:45   0:00 /sbin/getty 384
root       510  0.0  0.1  12740   848 tty2     Ss+  20:45   0:00 /sbin/getty 384
root       517  0.0  0.6  63876  3340 ?        Ss   20:45   0:00 sshd: cabox [pr
cabox      519  0.0  0.2  64172  1540 ?        S    20:45   0:00 sshd: cabox@not
cabox      520  0.0  0.1  12916  1016 ?        Ss   20:45   0:00 /usr/lib/openss
root       931  0.0  0.6  63876  3476 ?        Ss   21:21   0:00 sshd: cabox [pr
root       932  0.0  0.6  63876  3476 ?        Ss   21:21   0:00 sshd: cabox [pr
cabox      935  0.0  0.2  63876  1464 ?        S    21:22   0:00 sshd: cabox@pts
cabox      936  0.0  0.2  63876  1464 ?        S    21:22   0:00 sshd: cabox@pts
cabox      937  0.0  0.8  20632  4556 pts/1    Ss+  21:22   0:00 -bash
cabox      945  0.0  0.8  20632  4552 pts/2    Ss+  21:22   0:00 -bash
root      2177  0.0  0.6  63876  3476 ?        Ss   22:32   0:00 sshd: cabox [pr
cabox     2179  0.0  0.2  64008  1484 ?        S    22:32   0:00 sshd: cabox@pts
cabox     2180  0.0  0.8  20632  4556 pts/0    Ss   22:32   0:00 -bash
cabox     2387  0.0  0.2  15520  1140 pts/0    R+   22:45   0:00 ps aux
cabox@box-codeanywhere:~/workspace/challenge_files$ ps aux | grep cabox
root       517  0.0  0.6  63876  3340 ?        Ss   20:45   0:00 sshd: cabox [pr
i
