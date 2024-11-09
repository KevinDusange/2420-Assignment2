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

In your case it will be convenient to use -a to run all the scrips at once using the format below.

```
sudo ./main_script -a
```



### Project 2
