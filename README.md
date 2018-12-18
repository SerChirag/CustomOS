# Welcome to CustomOS

Hi! This tool eases the proces of installing softwares. Currently I am focussing on :

 1. apt packages
 2. pip packages
 3. npm packages
 4. Some necessary softwares needed for everyday survival

# apt packages

First of all list all the manually installed packages. Run this command : 

    comm -23 <(apt-mark showmanual | sort -u) <(gzip -dc /var/log/installer/initial-status.gz | sed -n 's/^Package: //p' | sort -u) > package.txt
  
 This creates  a file containing all you packages. To install these packages on your new installation, run : 

    xargs -a package.txt sudo apt-get install

# pip packages

The file explorer is accessible using the button in left corner of the navigation bar. You can create a new file by clicking the **New file** button in the file explorer. You can also create folders by clicking the **New folder** button.

#  npm packages


