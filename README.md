remote desktop installed but rdp shows black screen when logging in :

To solve this issue, there is a simple fix.  You need to ensure the account you are using to login via the remote 
desktop client is not currently logged on locally on the Ubuntu target machine. 
If this is the case, perform a logout operation as shown in the screenshot below….

run a show users with:
#who -u

that give you the PID

Then you can kill the user session.

kill "pid"
now run rdp again
once you see the desktop hit cancel on the password
