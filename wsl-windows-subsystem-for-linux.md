# Welcome to WSL/WSL2 Install Experience

I have a windows 10 home and dont want to give up on server capabilities just yet. Wanted to checkout what would help convert this to a server
for my learning hobbies . One option is to spinup a VM and run it in bridged mode but that would not integrate well with all the dev tools 
on the host operating system. Wanted a seamless experience and then voila stumbled upon wsl/wsl2

As a first step wsl is auto installed by enabling features in
>Turn Windows Feature on or off 

control panel app (can be launched by typing the same in the **"Type here to search"** bar)

Features to Turn on 
>          - "Windows Subsystem For Linux"
>          - "Virtual Machine Platform"

This would get one up to the initial version of wsl .
Now to get the latest and greatest wsl experience one has to install  
**WSL2 Linux kernel update package for x64 machines**
from 

>https://docs.microsoft.com/en-us/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package

Now to start experiencing WSL2 install one of the linux distributions from 
>https://aka.ms/wslstore

I chose the ubuntu from canonical 

To set the default WSL to version 2 , 
run the below command from windows powershell

>wsl --set-default-version 2

If you get an error like the one below
>Error: 0xc03a001a while installing wsl2 distribution

You need to make sure to disable compression for the folder

>C:\Users\<username>\AppData\Local\Packages\<linux-distro>

make sure to replace  **\<username>** and the **\<linux-distro>** fillers above 
for example my ubuntu **\<linux-distro>** at the time of writing this was 
>CanonicalGroupLimited.Ubuntu20.04onWindows_79rhkp1fndgsc

now launch the downloaded application again and 
it should seek information like the new **username** and **password** 
for the linux environment and finish successfully

Now to confirm the linux distros from the windows powershell 
run the below command

>wsl -l -v

# Thats all folks !!!! 
