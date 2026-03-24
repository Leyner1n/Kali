# [[Directory and File Management]]


**cd** - Move to (directory)


**cat** - Command to read and output file contents

**echo** - Show in terminal 

**grep**  - Search txt (grep "word")

**sort** - sorting (-n = by numbers, -r = reverse, 
-u = removing repetitions) 
![[Screenshot 2026-03-23 at 1.29.06 AM.png]]

## sudo 
	sudo - Granting root rights for one command
	
	su - by default switch to root (if u have password to root)
	su [options] [username]
	
	sudo passwd root - set passwort to root

	sudo -l - check ur rights

## fdisk  

	sudo fdisk (options) (disk)
	
	fdisk -l = disks list 

![[Screenshot 2026-03-23 at 2.42.39 AM.png]]



# User 
**id** - shows who r u and ==what kind of groups u have==(**"groups"**)
![[Screenshot 2026-03-23 at 2.18.00 AM.png]]

**who (w)** - Shows who in system now

**last** - Shows who was in system last 10 logs

**useradd** - Add user
![[Screenshot 2026-03-23 at 2.47.08 AM.png|560]]
`passwd [username who needs to change password]`

**usermod** - Using to edit user settings

**userdel** - Delete user
![[Screenshot 2026-03-23 at 3.09.09 AM.png]]

# Tools  

**"< or >"**  - Output redirection
**"<< or >>"** - Append output 
**"-i"** - gives interactive to use command 
**" | " (pipe)** - Transmits command 
**"~"** - /home/"username"
