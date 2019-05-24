
_created by it-slav Peter Andersson, peter.andersson@suse.com_


## Prepare
Hint:
cf help -a

## Demo
Login to CAP
cf login -a  https://api.cap.suselinux.info --skip-ssl-validation -u <USERNAME>
cf create-space test
cf target -o "YOURORG" -s "test"

Demo 1, deploy DizzyLizard from git
Login to stratos https://stratos.cap.suselinux.info
Click->Applications
Click->Top right ~~corner-arrow up~~ plus button ?

Organisation: <YOURORG>
Space: <YOURCREATED SPACE>
Click->Next

Source Type: Public GitHub <DEFAULT>
Project: scf-samples/dizzylizard
Branch: scf
Click->Next

Pick the first commit: Default disk allocation
Click->Next

Check: Create a random route
Leave the rest
Click->Deploy

Follow the logstream and explain what is happening

## CLEAN UP 
cf delete –r –f <appname> 
Figure out how to delete a service, hint cf help -a
