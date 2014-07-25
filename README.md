Connect code by Jay Pike

This is a simple, but lengthy, chunk of code designed to handle just
about type of ssh/telnet connection to a unix server.  There are also a
bunch of additional functions that this provides that assist in
administration.  You can also customize local functions for it to use as
well.  This is nearly 10 years old at this point but I use it all day
every day.

Supported Platforms:

	SunOS/Solaris 5.9/5.10
	Linux/RHEL: 4.* and newer

Requires:

	Expect installed locally and available in your $PATH

Here is the command line usage for it:

	regex:pikej05:[10:53am]:~> connect
	Syntax Error: No server specified!
	         /home/pikej05/bin/connect [options] host1 host2 host3 . . .
	        Options:
	         <-interact> - Interact with remote host
	         <-passwd> - Prompt the user for a new password to set on remote host
	         <-runcmd [cmd]> - Run the listed cmd on the remote host
	         <-sudo [cmd]>  - Run the listed cmd with sudo on the remote host
	         <-pbrun [cmd]>  - Run the listed cmd with pbrun on the remote host
	         <-user [username]> - Connect using the supplied username
	         <-password> - Force password prompting
	         <-debug> - Enable debug mode
	         <-timeout> [seconds] - Set the connection timeout in seconds
	         <-telnetfirst> - Try telnet before ssh (default is to use ssh first)
	         <-notelnet> - Do not try telnet(default is to use ssh first)
	         <-logfile [log file]> - Use the listed logfile rather than the default name
	Admin Functions:
	         admin-connect [options] host1 host2 host3 . . .
	        Options:
	         <-useraudit> - Create a list of all users on the server and last login dates
	         <-updatesudoers [updatesudoersfile]> - Process the listed file for sudoers updates
	         <-adminusers [usersfile]> - Process the listed file for user administration
	                         <-noaccountexpiry> - Don't force passwd change and no expiry info
	                         <-group> - default group name to use
	                         <-home> - default home directory to use. Ex: /export/home
	                         <-defaultpassword [default password to use]>
	         <-centrifyadminusers [usersfile]> - Process the listed file for user administration in both
	                non-Centrify and Centrified hosts
	                         <-noaccountexpiry> - Don't force passwd change and no expiry info
	                         <-group> - default group name to use
	                         <-home> - default home directory to use. Ex: /export/home
	                         <-defaultpassword [default password to use]>
	         <-compareusernames [usersfile]> - Compare usernames on the server those listed in usersfile
	         <-geteditsudoers> - Get the editsudoers.pl file from the source server
	         <-getfile [filename]> - Transfer local 'filename' to remote host using ftp
	         <-changepassword> [username] - Change the password and expiry options for an account back to the defaults
	                         <-noaccountexpiry> - Do not set account expiration information
	                         <-removeaccountexpiry> - Remove account expiry info
	                         <-noforcepasswordchange> - Do not force the user to change the password at the next login
	                         <-randomnewpassword> [random new password logfile] - Change the password to a random password and output info to the specified logfile
	                         <-group> - default group name to use
	                         <-defaultpassword [default password to use]>
	Alias Functions:
	         <alias function name> [options] host1 host2 host3 . . .
	regex:pikej05:[10:53am]:~> 
	
