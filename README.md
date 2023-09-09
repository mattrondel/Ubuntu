Plex server issues and fixes:
Plex is offline even after mount -a and sudo service plexmediaserver restart doesnt work 
every X days plex need a reauthorization using its credentials, so you will need to console in or use a physical monitor to re-authoriza the session

Issue:
Remote desktop is installed but rdp shows black screen when logging in :

To solve this issue, there is a simple fix.  You need to ensure the account you are using to login via the remote 
desktop client is not currently logged on locally on the Ubuntu target machine. 
If this is the case, perform a logout operation as shown in the screenshot below….
Using ssh :
run a show users with:
#### who -u

that give you the PID

Then you can kill the user session. not the tty one but any other one there

#### kill "pid"
now run rdp again
once you see the desktop hit cancel on the password
activities> firefox > open plex > open plex or login
try it aagin on the client side
once working restart the system through putty

Supposedly this will fix it but I am not ready to break something yet...
https://askubuntu.com/questions/1155053/remote-connecting-to-ubuntu-18-04-from-windows-remote-desktop-login-failed-for
