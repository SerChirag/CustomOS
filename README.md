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

To freeze the currently installed packages in your old installation, run this : 

    pip freeze > pip-packages.txt

To install : 

    pip install -r pip-packages.txt

#  Survival Kit

 1. 
	Proxy-Man, one proxy to rule them all : 
		
		https://github.com/himanshub16/ProxyMan
 2. 
	My dirt-laundary : 

	    git clone https://github.com/SerChirag/keylogger


#  Fonts

 1. Download the fonts folder, and rename it .fonts
 2. Move it to "Home directory"

