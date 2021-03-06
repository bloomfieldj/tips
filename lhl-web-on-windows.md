# Using Windows for LHL Web Dev

### Big thank you to Habib, [Yves](https://github.com/ycandau), [Andrew](https://github.com/ahSOLO) and Adam
### https://web-prep-help.lighthouselabs.ca/t/win10-users-setup-tutorials-setup-info-dump/7031/

## AMD CPU Users start here: 

Boot into BIOS and enable Secure Virtual Machine Mode (SVM) then proceed to the next steps.


## Install VirtualBox for Windows
https://www.virtualbox.org/wiki/Downloads

## Install Vagrant for Windows

https://www.vagrantup.com/downloads 

## Install Windows Terminal

https://www.microsoft.com/en-ca/p/windows-terminal/9n0dx20hk701? 

## Install Git Bash

1.	https://git-scm.com/download/win 

2.	During installation, select the option to add it to Windows Terminal

##	Set Git Bash as Default in Windows Terminal

## Setting up "lighthouse folder"	

1. Create "lighthouse" folder somewhere convenient like Desktop or Documents

2. Open Windows Terminal

3. Open Settings 

4.	Navigate to Git Bash under Profiles

5.	Change Starting Directory for Git Bash to your "lighthouse" folder

##	Download Vagrant File to your lighthouse folder

1.	Open a Git Bash tab using Windows Terminal

2.	curl -O http://d10ofk0qhbh8u9.cloudfront.net/vagrant/Vagrantfile

##	Connect to VM

1.	make sure you're in the "lighthouse" folder

2.	vagrant up

3.	vagrant ssh

## Head back to Compass to connect your GitHub account!

## To prevent symlink issues when installing packages with npm
Always run Windows Terminal as Administrator

## To set node env variables
Update package.json file script with SET and &&.

SET: Assigns value to a variable

&&: Tells windows to run consecutive commands, careful not to leave a space between the first command and the &&

### Before
```
"scripts":
    "error": "TEST_ERROR=true node ./src/index.js"
}
```
![Default script](https://github.com/bloomfieldj/tips/blob/main/env.jpg?raw=true)

### After 

```
"scripts":
    "windowserror": "SET TEST_ERROR=true&& node ./src/index.js"
}
```
![Windows script](https://github.com/bloomfieldj/tips/blob/main/envfix.jpg?raw=true)
