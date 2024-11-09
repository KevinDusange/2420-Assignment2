# 2420-Assignment-2

#### Overview

In this guide we will be creating 2 different projects for initial system setup and to create new users. For Project 1 (initial system setup) the scripts will install essential packages as well as create symbolic links. For Project 2 (new user creation) the scripts will automate the process of creating a new user and giving that user a new password. 


## Projects

### Project 1 - System Setup Scripts

There are three scripts for this project as wel as one txt file that contains which pakcages needed to be installed.

1. Install Package Script: Script to install system packages from the packages.txt file
2. Symbolic Link Script: Script to create symbolic links from the configuration files from the cloned repo.
3. Main Script: This script first clones the repo and then runs the other two scripts to complete them both at once.
4. Package List: A simple txt file that contains the packages we need

#### To run this project

You will need to download all the scripts to your system including the txt file. Once you have the files you only need to run the main script. To run this script use the format below:

The options you can give to this command are -p, -s, or -a.
- -p will only install the packages
- -s will only create the symbolic links
- -a will install the packages and create the symbolic links

The most convenient way to use this script would be to use -a to run all the scrips at once using the format below.

```
sudo ./main_script -a
```

This will install the packages and create the symbolic links.


### Project 2 - New User Creation

In this project script we will be automating the process of creating a new user. We will give the user the option to enter a username, a password, as well as their preferred shell. The script will automatically create the user, the home directory for that user, and configure the group memberships. 

There is only one script neede to automate this process. The user_script script. The format to run this script is:

```
sudo ./user_script -u <new-username> -p <new-password> -s <preferred-shell>
```

This script will:
1. Take in the options using OPTARG and save them in their respectable variables
2. Create a User ID and a matching Group ID
3. Update the password using chpasswd (after the user is created)
4. Update the entries in the /etc/passwd and /etc/groups files

Once the user has been created you can double check by running the command:

```
cat /etc/passwd
```

You will see the new user you just created at the bottom of this list in the following format:

```
<username>:x:<user-id>:<group-id>::/home/<username>:<shell>
ex. kevin4:x:1003:1003::/home/kevin4:/bin/bash
```

####
- An initial system setup with packages installed and configuration files linked.
- The ability to add new users with a secure password and specific shell settings.
- These projects will automate the system setup and new user creation.

#### Notes

- Remeber to make sure the scripts can be executable by using `chmod +x <script-name>`
- Also remember to run these scripts using sudo or root privelages ex. `sudo ./<script-name>`
- These scripts are made to be used on Linux based systems

### References

- https://gitlab.com/cit2420/2420-notes-f24/-/blob/main/2420-notes/week-four.md
- https://gitlab.com/cit2420/2420-notes-f24/-/blob/main/2420-notes/week-five.md
- https://gitlab.com/cit2420/2420-notes-f24/-/blob/main/2420-notes/week-six.md
- https://gitlab.com/cit2420/2420-notes-f24/-/blob/main/2420-notes/week-seven.md
- https://phoenixnap.com/kb/how-to-list-users-linux
- https://phoenixnap.com/kb/chpasswd
- https://linuxize.com/post/how-to-create-symbolic-links-in-linux-using-the-ln-command/
- https://linuxize.com/post/linux-chown-command/
- https://devhints.io/bash
- https://stackoverflow.com/questions/714915/using-the-passwd-command-from-within-a-shell-script