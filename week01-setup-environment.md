In the first session, you need to set up your environment and learn to use basic tools. This includes accessing a Linux server, configuring SSH keys, using Bash, and working with the Vim editor.

#### Preliminary notes
- The Command Line Interface (CLI) is a powerful alternative to the Graphical User Interface (GUI) for operating system interaction. For the user, it appears as a command prompt (shell) where commands can be typed. Additionally, it allows creating scripts that group commands together, enabling more complex behavior. Mastery of the CLI is essential knowledge for any programmer. 
- In the Linux operating system, unlike many other operating systems, all commands are thoroughly documented. To access the help documentation for any command, one must utilize the `man` command. It is noteworthy that `man` stands for manual, and it is possible to invoke `man` even for itself.
- Command-line utilities also typically display explanations on the screen in the event of errors. It is crucial to read what they output, as this serves as a primary source of information, alongside the man pages.
- Upon opening a terminal, the cursor is typically positioned not at the first character of the line, but after a specific prompt. These prompts can vary, often displaying the username, the name of the server or computer, and the current directory. My prompt:
```
	(base) kirill@box:~/Projects$
```
- Crucially, each prompt concludes with either a dollar sign or a hash symbol. The dollar sign ($) indicates that the user is a regular user, whereas the hash symbol (#) signifies that the user has super-power, its name is always **root**. 
- Each user has a designated home directory. To navigate to the home directory, one must type `cd` without any arguments. To view the current directory, the command `pwd` should be used. In file paths, when referencing files, the home directory can be substituted with the tilde symbol (`~`).
- Please read all this file till the end and use man to study all mentioned command before following the instructions.
#### Step by step instruction

- In browser follow the [link](https://getlinux.csai.site/) and request access to remote Linux machine. It will ask you to do authorization via github and show username, password, server name and port of the server
	- ! IMPORTANT: Do not store any important files on the server, it does not have any backup or data protection mechanism. It is a good idea to keep everything in git (github).
- After getting password wait for 1 minute while user is being created and password set.
- Open terminal program on your local machine
	- in Linux, I recommend to install *terminator* instead of default one
	- in Windows - cmd
	- in MacOS - terminal
- Connect to the remote server via ssh and type (or insert the password)
```
	$ssh -p PORT username@server_name
```
- For detailed instructions how to work with ssh use `man ssh` :)
- On the local machine generate key pair: private and public keys.
```
	$ssh-keygen
```
- You can specify file name for keys or use suggested default. Do not set the password for new key pair.
- Login again to the server via ssh with password and create ~/.ssh directory or check if it exist
- From the local machine copy your public key to remote server. For this you can use the following command
```
	$scp -P port public_key username@server_name:/destination/directory
```
- Use 'cat' with '>' or cp command to copy public key file content to file ~/.ssh/authorized_keys
- Now you can connect from local machine to remote server with your private key without password, but you need to specify your private key as your identity file:
```
	$ssh -p PORT -i /path/to/your/private/key username@server_name
```
- For the convenience, you can also describe a connection in your ~/.ssh/config file. It allows you only to specify myserver as only argument for 'ssh' This is an example:
```
	Host          myserver
    HostName      192.168.10.107
	User	      kirill
	IdentityFile  ~/.ssh/id_ed25519
	Port          9921
```
- Connect to the remote server and complete vimtutor for mastering with vim
- You can use terminal multiplexer 'tmux' to keep your remote environment even if you disconnected from the remote machine.
#### What would help
- ChatGPT, search engines like google, bing, etc
- 'man' for man, ssh, ssh-keygen, scp, tmux
- [Linux Bash Shell Cheat Sheet](https://oit.ua.edu/wp-content/uploads/2020/12/Linux_bash_cheat_sheet-1.pdf)
- [Vim cheat sheet](https://web.stanford.edu/class/cs110/summer-2021/handouts/vim-cheat-sheet/)
- [Tmux Cheat Sheet & Quick Reference](https://tmuxcheatsheet.com/)
#### Stuck with something?
- Ask a question in the class chat, everybody welcome to answer and help
- Tag @krinkin if the problem too unclear how to approach
#### Want to contribute of found a bug?
- Feel free to clone [the repo](https://github.com/programming-fundamentals-class/supplementary-2024), send a pull request

