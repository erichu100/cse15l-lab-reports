# Installing VSCode
![Image](vsInstall.png)
* Install VSCode from its website [here](https://code.visualstudio.com/).
* Used as a code editor and includes a terminal that can be used as a console.
# Remotely Connecting
![Image](remotelyConnecting.png)
* Can remotely connect to servers using the ssh command.
* In this case, url found by UCSD [account lookup] (https://code.visualstudio.com/)
    * cs15lwi22ail@ieng6.ucsd.edu
* Requires a password or a SSH key.
# Trying Some Commands
![Image](commandTest.png)
* Can use same commands as local system.
* Examples: `cd` (change directory), `ls` (list), `cp` (copy), `cat` (con cat enate). 
# Moving Files with `scp`
![Image](sshTest.png)
* Can transfer files from local machine to remote machine with `scp` command.
* scp  _File-Name_  _ServerUrl_.
    * Must be run on local machine.
# Setting an SSH Key
![Image](keyGeneration.png)
* Can generate a key on your computer with `ssh-keygen`.
* Create an .ssh directory on remote server.
* `scp` the key from your computer to the remote server.
# Optimizing Remote Running
![Image](sshShortcuts.png)
* Can use quotes to quickly run commands after `ssh`, but will return to local machine after the end quotes.
* Semicolons string together commands in one line.