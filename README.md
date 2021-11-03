# born2beroot
born2beroot project

Some Important Observations:

To resolve the permission issue: **`sudo chmod 777 wp-content/`**

Should not use "@" symbol in password to login to ftp

While cloning uncheck ip address not change it 

check root, user password rules using : sudo chage -l <root>

sudo chage -l <username> etc.

Port 21 → for FPT

Port 80 → for wordpress website access

Leave only port 42 and 42(v6) open before evaluation. (sudo ufw status)

Only Follow the below 2 Tutorials to set up the vitual mechine. Not knowing and following other tutorials will be a trouble later. 

Basic part:

[https://github.com/HEADLIGHTER/Born2BeRoot-42/blob/main/walkthrough37.txt](https://github.com/HEADLIGHTER/Born2BeRoot-42/blob/main/walkthrough37.txt)

Bonus part:

[https://githubmemory.com/repo/hanshazairi/42-born2beroot](https://githubmemory.com/repo/hanshazairi/42-born2beroot)

Suggested install location: 1-D-14 ->Macintosh HD -> goinfre -> amathew

Suggestions:

1. in the setting for VirtualBox (in this top menue of the Mac) set the "goinfre" as standard folder!
2. When setting up the machine, under network, choose bridged adapter
3. do the complete basics an the HD setup like HEADLIGHTER, complete HD size 8.6G
4. walk throug the complete process of HEADLIGHTER
5. Do a snapshot in virtualbox (or more if you are not shure doing the things the right way), at least before you start bonus part
6. test the ssh thing with the local IP-Address of your debian machine, youm may encounter probs there, because you have a new machine. Google helps.
7. Follow this hanshazari steps for bonus
8. setup the WP, be orientated about the Passwords you set to the different things (don't do the things with emptiness in your eyes )
9. login to the admin of the WP site
10. try to configure the site, e.g. try to configure the "favicon", you may experience probs with access rights
11. setup "htop" as second service
12. do testings
13. check the PWD rule for root user ect
14. generate a CLONE of the machine to get rid of the snapshot mode, you may run in probs if you didn'n follow Point1!

[34 Linux Basic Commands Every User Should Know](https://www.notion.so/34-Linux-Basic-Commands-Every-User-Should-Know-bae7915a45ab4afe84c2cb13889f24f6)

**Born2beroot**

Most Important : user password should not contain @ symbol otherwise, ftp will not get connected

[https://www.technoduet.com/a-simple-way-to-connect-to-remote-ftp-sever-on-mac/](https://www.technoduet.com/a-simple-way-to-connect-to-remote-ftp-sever-on-mac/)

**Born2beRoot Project Requirements:**

1. 	Ensure that the "signature.txt" file is present at the root of the cloned repository.

**cd /goinfre/amathew**

**shasum born2beroot.vdi**

2.	Check that the signature contained in "signature.txt" is identical to that of the ".vdi" file of the virtual machine to be evaluated. A simple "diff" should allow you to 	compare the two signatures. If necessary, ask the student being evaluated where their ".vdi" file is located. (diff file1.txt file2.txt)

1. 3.	As a precaution, you can duplicate the initial virtual machine in order to keep a copy.
2. 4.	Start the virtual machine to be evaluated.

Mandatory part:

1. 1.	How a virtual machine works?
2. 2.	My choice of operating system
3. 3.	The basic difference between CentOS and Debian
4. 4.	The purpose of virtual mechine
5. 5.	The difference between aptitude and apt and what is APPArmor?
6. 6.	A script must disply every 10 minutes. (sudo crontab -e ,
7. 7.	Ensure that the machine does not have a graphical environment at launch.
8. 8.	A password will be requested before attempting to connect to this machine.

Finally, connect with a user with the help of the student being evaluated. This user must not be root.

1. 9.	Pay attention to the password chosen, it must follow the rules imposed in the subject.
2. 10.	Check that the UFW service is started with the help of the evaluator.
3. 11.	Check that the SSH service is started with the help of the evaluator.
4. 12.	Check that the chosen operating system is Debian or CentOS with the help of the evaluator.

User:

1. 1.	The subject requests that a user with the login of the student being evaluated is present on the virtual machine.
2. 2.	Check that it has been added and that it belongs to the "sudo" and "user42" groups.
3. 3.	Make sure the rules imposed in the subject concerning the password policy have been put in place by following the following steps.
4. 4.	First, create a new user. Assign it a password of your choice, respecting the subject rules. The student being evaluated must now explain to you how they were able to set up the rules requested in the subject on their virtual machine.
5. 5.	Normally there should be one or two modified files. If there is any problem, the evaluation stops here.
6. 6.	Now that you have a new user, ask the student being evaluated to create a group named "evaluating" in front of you and assign it to this user. Finally, check that this user belongs to the "evaluating" group.
7. Finally, ask the student being evaluated to explain the advantages of this password policy, as well as the advantages and disadvantages of its implementation. Of course, answering that it is because the subject asks for it does not count.

Hostname and partitions :

1. 1.	Check that the hostname of the machine is correctly formatted as follows: login42 (login of the student being evaluated).
2. 2.	Modify this hostname by replacing the login with yours, then restart the machine. If on restart, the hostname has not been updated, the evaluation stops here.
3. 3.	You can now restore the machine to the original hostname.
4. 4.	Ask the student being evaluated how to view the partitions for this virtual machine.
5. 5.	Compare the output with the example given in the subject. Please note: if the student evaluated makes the bonuses, it will be necessary to refer to the bonus example.
6. 6.	his part is an opportunity to discuss the scores! The student being evaluated should give you a brief explanation of how LVM works and what it is all about.

Sudo:

1.Check that the "sudo" program is properly installed on the virtual machine.

1. 2.	The student being evaluated should now show assigning your new user to the "sudo" group.
2. 3.	The subject imposes strict rules for sudo. The student being evaluated must first explain the value and operation of sudo using examples of their choice.
3. 4.	In a second step, it must show you the implementation of the rules imposed by the subject.
4. 5.	Verify that the "/var/log/sudo/" folder exists and has at least one file. Eg: sudo apt udate then sudo cat log_details
5. 6.	Check the contents of the files in this folder,
6. 7.	You should see a history of the commands used with sudo.
7. 8.	Finally, try to run a command via sudo. See if the file (s) in the "/var/log/sudo/" folder have been updated.

Wordpress login: 

[http://10.11.250.134/wp-login.php?redirect_to=http%3A%2F%2F10.11.250.134%2Fwp-admin%2Ftheme-install.php%3Fbrowse%3Dpopular&reauth=1](http://10.11.250.134/wp-login.php?redirect_to=http%3A%2F%2F10.11.250.134%2Fwp-admin%2Ftheme-install.php%3Fbrowse%3Dpopular&reauth=1)

# **Table of entries**

- [General guidelines](https://github.com/Arrtthhuur/Born2beRoot#guide)
- [VMs](https://github.com/Arrtthhuur/Born2beRoot#vm)
- [OS](https://github.com/Arrtthhuur/Born2beRoot#os)
- [Hostname](https://github.com/Arrtthhuur/Born2beRoot#host)
- [Encrypted partitions](https://github.com/Arrtthhuur/Born2beRoot#encrypt)
- [Graphical](https://github.com/Arrtthhuur/Born2beRoot#graph)
- [sudo](https://github.com/Arrtthhuur/Born2beRoot#sudo)
- [SSH](https://github.com/Arrtthhuur/Born2beRoot#ssh)
- [UFW](https://github.com/Arrtthhuur/Born2beRoot#ufw)
- [Password policy](https://github.com/Arrtthhuur/Born2beRoot#pass)
- [Monitoring script](https://github.com/Arrtthhuur/Born2beRoot#script)
- [Bonus](https://github.com/Arrtthhuur/Born2beRoot#bonus)
- [Eval Cheat Sheet](https://github.com/Arrtthhuur/Born2beRoot#ecs)

## **Subject / Eval sheet**

- [subject.pdf](https://github.com/Arrtthhuur/Born2beRoot/blob/main/Born2beroot.pdf#section)
- [eval_sheet.pdf](https://github.com/Arrtthhuur/Born2beRoot/blob/main/eval_sheet_b2br.pdf#section)

## **General guidelines**

- The use of **VirtualBox** (or UTM if you can’t use VirtualBox) is **mandatory**.
- You only have to turn in a `signature.txt` file at the root of your repository. You must paste in it the signature of your machine’s virtual disk. Go to Submission and peer-evaluation for more information.

## **VMs**

- **During eval:** Explain simply:
    - How a virtual machine works.
    - The purpose of virtual machines.

### **Useful links**

- [THIS IS THE TUTORIAL I FOLLOWED TO INSTALL DEBIAN ON VM](https://www.brianlinkletter.com/2012/10/installing-debian-linux-in-a-virtualbox-virtual-machine/)
- [What is a VM?](https://azure.microsoft.com/en-us/overview/what-is-a-virtual-machine/#overview)
- [What is a VM?](https://www.vmware.com/topics/glossary/content/virtual-machine)

---

## **OS: Debian**

- **During eval:** Explain simply:
    - Their choice of operating system :
        
        to check installed operating system: **cat /etc/os-release**
        
        **Debian is highly recommended if somebody is new to system administration.**
        
    - **The basic differences between CentOS and Debian.**
        
        CentOS vs Debian are two flavors of Linux operating systems. CentOS, as said above, is a Linux distribution. It is free and open-source. It is enterprise-class – industries can use meaning for server building; it is supported by a large community and is functionally supported by its upstream source, Red Hat Enterprise Linux. Debian is a Unix like computer operating system that is made up of open source components. It is built and supported by a group of individuals who are under the Debian project. Debian uses Linux as its Kernel. Fedora, CentOS, Oracle Linux are all different distribution from Red Hat Linux and are variant of RedHat Linux. Ubuntu, Kali, etc., are variant of Debian. CentOS vs Debian both are used as internet servers or web servers like web, email, FTP, etc.
        
        # **Key differences between CentOS and Debian**
        
        Both servers are popular choices in the market; let us discuss some of the major difference:
        
        - One should pick [Debian](https://www.educba.com/what-is-debian/) as it generally has more up to date packages and because it is easier to upgrade to a newer version. A lot of people have started their GNU/Linux journey with Red Hat Linux, and they have always used CentOS and Fedora on their Desktop.
        - If one is more used to [CentOS](https://www.educba.com/what-is-centos/) and is more accustomed to working with it or have been using it for a long, then there is no real reason to migrate to Debian. CentOS vs Debian are both the best options one can have when choosing a GNU/Linux distribution to install on their web server or any other server.
        - There is one more thing that one should keep in mind when installing a Web Server. If this server is going to be used as a reseller tool, he/she may want to install a tool called cPanel, and in such a case going with CentOS is recommended, as it is officially supported.
        
        # **CentOS vs Debian Comparison Table**
        
        The primary comparison is discussed below:
        
        [Untitled](https://www.notion.so/23a3a1dcb4d346c484a97b51b2e252f1)
        
        # **Conclusion**
        
        This article covers almost all business-specific or choice-based reasons to differentiate between CentOS and Debian. Both are an excellent piece of software and is used by thousands of applications and many more developers. Both Debian vs CentOS of them are highly trusted by the industry and runs the core components of mission-critical applications. Hence it does not matter much which one is used in a given scenario. A developer can prefer which he is more comfortable with and about which he knows the most.   If a general guideline is to be provided, CentOS probably runs a number of servers currently than any other version of Linux.  For a beginner also, Learning and starting with CentOS makes more sense, and it provides better and more challenging career scope. Ubuntu is a major brownie point for Debian. From an administrator perspective also, CentOS wins in the majority of situations compared to Debian.
        
    - Debian: the difference between aptitude and apt, and what APPArmor is.

### **Useful links**

- [OS - Overview](https://www.tutorialspoint.com/operating_system/os_overview.htm)
- [CentOS vs Debian](https://www.openlogic.com/blog/centos-vs-debian)
- [CentOS vs Debian](https://www.educba.com/centos-vs-debian/)
- [CentOS vs Debian](https://1gbits.com/blog/debian-vs-centos/)
- [Aptitude vs apt](https://www.tecmint.com/difference-between-apt-and-aptitude/#:~:text=Apt%2Dget%20being%20a%20lower,operation%20by%20entering%20required%20commands.)
    
    **Apt : Advanced Packaging Tool** is a free and open source software which gracefully handles software installation and removal.
    
    It doen't hav a GUI
    
    Whenever invoked from command line along with specifying the name of package to be installed, it finds that package in configured list of sources specified in **‘/etc/apt/sources.list’** along with the list of dependencies for that package and sorts them and automatically installs them along with the current package thus letting user not to worry of installing dependencies.
    
    **Aptitude** is front-end to advanced packaging tool which adds a user interface to the functionality, thus allowing a user to interactively search for a package and install or remove it.
    
- [APPArmor](https://www.howtogeek.com/118222/htg-explains-what-apparmor-is-and-how-it-secures-your-ubuntu-system/)
    
    APPArmor is a security feature that silently runs in the background. To check the status of the APPArmor → **sudo apparmor_status**
    
    AppArmor allows  developers to restrict the actions processes can take.
    

---

## **Hostname**

> The hostname of your virtual machine must be your login ending with 42 (e.g., abeznik42).
> 

**ssh amathew@10.11.250.134 -p 4242**

# The procedure to find the hostname

1. Open a command-line terminal app (select Applications > Accessories > Terminal), and then type:
2. **hostname** OR
    
    **hostnamectl OR**
    
    **cat /proc/sys/kernel/hostname**
    
3. Press [Enter] key
- **During eval:**
    - Check that the hostname of the machine is correctly formatted as follows: login42 (login of the student being evaluated).
    - Modify this hostname by replacing the login with evaluator's login, then restart the machine. If on restart, the hostname has not been updated, the evaluation stops here.
    - You can now restore the machine to the original hostname.

### **[Changing hostname](https://github.com/Arrtthhuur/Born2beRoot/blob/main/hostname/README.md#section)**

Display the current hostname:

```
hostnamectl
```

Become root with `su`

To set the hostname to <server_name>, run:

```
hostnamectl set-hostname <server_name>
```

Edit the file `/etc/hosts` and replace all occurences of previous server_name by the new server name:

`nano /etc/hosts`

---

Question: Should I delete the local host?

## **Encrypted partitions**

> You must create at least 2 encrypted partitions using LVM. Below is an example of the expected partitioning:
> 

![https://user-images.githubusercontent.com/43698378/136699027-5a77000c-c0f0-4b78-8919-98be71d3e2b9.png](https://user-images.githubusercontent.com/43698378/136699027-5a77000c-c0f0-4b78-8919-98be71d3e2b9.png)

- **During eval:**
    - Show the partitions for this virtual machine.
        - Compare the output with the example given in the subject. Please note: if bonuses, refer to the bonus example.
    - Give a brief explanation of how LVM works and what it is all about.

Using the command `lsblk` will display the partitions.

### **[Encrypt partitions with LVM](https://github.com/Arrtthhuur/Born2beRoot/blob/main/lvm/README.md#section)**

---

## **No graphical interface**

> Since it is a matter of setting up a server, you will install the minimum of services. For this reason, a graphical interface is of no user here. It is therefore forbidden to install X.org or any other equivalent graphics server.
> 
- **During eval:**
    - Ensure that the machine does not have a graphical environment at launch.

Deselect **Desktop environment** and **GNOME** from **software selection** during the install in order to get a non-GUI Debian install.

---

## **sudo**

> To set up a strong configuration for your sudo group, you have to comply with the following requirements:
> 
> - Authentication using sudo has to be limited to 3 attempts in the event of an incorrect password.
> - A custom message of your choice has to be displayed if an error due to a wrong password occurs when using sudo.
> - Each action using sudo has to be archived, both inputs and outputs. **The log file** has to be saved in the **/var/log/sudo/ folder.**
> - The TTY mode has to be enabled for security reasons.
> - For security reasons the paths that can be used by `sudo` must be restricted. Example: `/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin`
- **During eval:**
    - Check that the "sudo" program is properly installed on the virtual machine.
        
        **sudo service --status-all**
        
    - Show assigning new user to the "sudo" group.
        
        ***How to add a new user?***
        
        sudo adduser <user_name>
        
        ***How to create a new group?***
        
        sudo addgroup <group_name>
        
        ***How to add a user to a group?***
        
        sudo usermod -aG <group_name> <user_name>
        
    - The subject imposes strict rules for sudo. First explain the value and operation of sudo using examples.
    
    `sudo visudo` -> sudo policy
    
    - Show the implementation of the rules imposed by the subject.
        
        Sudo is used for **Running *root*Privileged Commands**
        
    - Verify that the "/var/log/sudo/" folder exists and has at least one file.
        - Check the contents of the files in this folder, You should see a history of the commands used with sudo.
    - Run a command via sudo. See if the file(s) in the "/var/log/sudo/" folder have been updated.
    
    Common password policy: 
    
    sudo nano /etc/pam.d/common-password
    

### **[sudo installation & configuration](https://github.com/Arrtthhuur/Born2beRoot/blob/main/sudo/README.md#section)**

---

## **SSH service**

> A SSH service will be running on port 4242 only. For security reasons, it must not be possible to connect using SSH as root.
> 
- **During eval:**
    - Check that the SSH service is properly installed on the virtual machine.
    
    command→ **sudo service ssh status**
    
    - Check that it is working properly.
    - Explain to you basically what SSH is and the value of using it
    
    **Secure Shel**l or **Secure Socket Shell**, is a [network protocol](https://searchsecurity.techtarget.com/definition/Secure-Shell) that gives system administrators a secure way to access remote assets over an unsecured network.
    
    **SSH protocol** is built into Unix and Linux servers to enable secure connections between systems.
    
    - Verify that the SSH service only uses port 4242.
        
        **sudo nano /etc/ssh/sshd_config**
        
    - Use SSH in order to log in with the newly created user.
        - you can use a key or a simple password.
        - make sure you cannot use SSH with the "root" user.

### **[SSH installation & configuration](https://github.com/Arrtthhuur/Born2beRoot/blob/main/ssh/README.md#section)**

---

## **UFW firewall**

> You have to configure your operating system with the UFW firewall (Uncomplicated FireWall) and thus leave only port 4242 open.
> 
- **During eval:**
    - Check that the "UFW" program is properly installed on the virtual machine.
    - Check that it is working properly.
    - Explain to you basically what UFW is and the value of using it.
    - List the active rules in UFW. A rule must exist for port 4242.
    - Add a new rule to open port 8080. Check that this one has been added by listing the active rules.
    - Finally, delete this new rule with the help of the student being evaluated.

### **[UFW installation & configuration](https://github.com/Arrtthhuur/Born2beRoot/blob/main/ufw/README.md#section)**

---

## **Strong password policy**

> To set up a strong password policy, you have to comply with the following requirements:
> 
> - Password has to expire every 30 days.
> - Minimum number of days allowed before modification of a password will be set to 2.
> - User has to receive a warning message 7 days before their password expires.
> - Password must:
>     - be at least 10 characters long
>     - contain an uppercase letter and number
>     - **not** contain more than 3 consecutive identical characters
>     - **not** include the name of the user
>     - **does not apply to root password**: have at least 7 character that are **not** part of the former password
>     - **does apply to root password**: after setting up config files, you will have to change all the passwords of the acounts present on the VM.
- **During eval:**
    - Explain advantages of this password policy.
    - Explain advantages and disadvantages of its implementation.

### **[Strong password installation & configuration](https://github.com/Arrtthhuur/Born2beRoot/blob/main/passwd/README.md#section)**

---

## **User**

> In addition to the root user, a user with your login as username has to be present. And has to belong to sudo and user42 groups.
> 

To delete the user, without removing the user files, run:

```
sudo deluser usernameCopy
```

If you want to delete the user and its home directory and mail spool, use the `--remove-home` flag:

```
sudo deluser --remove-home username
```

- **During eval:**
    - A user with the login of the student being evaluated has to be already present on the virtual machine.
        - Check that it has been added and that it belongs to the "sudo" and "user42" groups.
    - Make sure the rules imposed in the subject concerning the password policy have been put in place by following the following steps.
        - Create new user.
        - Assign password of choice (respecting rules) and explain how these rules were set up. (there should be one or two modified files)
        - Create a group named "evaluating" and assign it to this user.
            - Finally, check that this user belongs to the "evaluating" group.

### **[Users, groups, ...](https://github.com/Arrtthhuur/Born2beRoot/blob/main/user/README.md#section)**

---

## **Monitoring script**

> monitoring.sh developped in bash.At server startup, the script will display some information on all terminals every 10min (see wall), banner is optional, no error must be visible.Following information must be displayed:Architecture of your OS and its kernel versionThe number of physical processors.The number of virtual processors.The current available RAM on your server and its utilization rate as a percentage.The current available memory on your server and its utilization rate as a percentage.The current utilization rate of your processors as a percentage.The date and time of the last reboot.Whether LVM is active or not.The number of active connections.The number of users using the server.The IPv4 address of your server and its MAC (Media Access Control) address.The number of commands executed with the sudo program.
> 
- **During eval:**
    - How the script works, by showing the code.
    - What "cron" is.
    - How it was set up so that it runs every 10min.
    - Ensure that this script runs every minute, make sure that the script runs with dynamic values correctly.
    - Make the script stop running when the server has started up, without modifying the script itself. (you'll have to restart one last time)
    - At startup, check if the script still exists in the same place, rights have remained unchanged, and not been modified.
- Example below:

![https://user-images.githubusercontent.com/43698378/136701814-cc671d24-9bd5-4d6f-8d89-bb2c19d4d6e9.png](https://user-images.githubusercontent.com/43698378/136701814-cc671d24-9bd5-4d6f-8d89-bb2c19d4d6e9.png)

### **[Monitoring script](https://github.com/Arrtthhuur/Born2beRoot/blob/main/script/#section)**

---

## **Bonus (work in progress)**

Network adapter configuration

You may not be able to connect to your VM via SSH with standard settings in VirtualBox. Theres a way to wix it!

1. Turn off your VM
2. Go to your VM settings in VirtualBox
3. Network -> Adapter 1 -> Advanced -> Port forwarding
4. Add new rule (little green button on right top side) and next parameters:

[Untitled](https://www.notion.so/38f2f0c2dc8040af9a17ee5e1ebbf95a)

1. In your host (physical) machine open Terminal and run

```
[ssh <vmusername>@localhost -p 4242]
```

Now you can control your virtual machine from the host terminal.

### **Useful links**

- [lighttpd](https://www.rosehosting.com/blog/how-to-install-lighttpd-on-debian-9/)
- [WordPress](https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-with-lamp-on-debian-9)

---

## **Eval Cheat Sheet**

For the eval, since you have to compare the signature.txt in your git with the signature of the VM you're doing the eval on, I made a ***snapshot*** of my VM. And I would just have to reset the initial state of the snapshot after the eval, and I would therefore have the same signature for all 3 evals. ez pz.

![https://user-images.githubusercontent.com/43698378/136701852-a3309cc5-fae6-4d6e-9ca5-939b0ad138f2.png](https://user-images.githubusercontent.com/43698378/136701852-a3309cc5-fae6-4d6e-9ca5-939b0ad138f2.png)

1. `head -n 2 /etc/os-release` -> display OS
2. `ss -tunlp` -> display sockets
3. `lsblk` -> check partitions
4. `sudo aa-status` -> AppArmor status
5. `getent group sudo` -> sudo group users
6. `getent group user42` -> user42 group users
7. `sudo service ssh status` -> ssh status

1. `sudo ufw status` -> ufw status
2. `ssh username@ipadress -p 4242` -> connect to VM from your host (physical) machine via SSH
3. `sudo visudo` -> sudo policy
4. `nano /etc/login.defs` -> password expire policy
5. `nano /etc/pam.d/common-password` -> password policy
6. `sudo crontab -l` -> cron schedule

***How to add a new user?***

```
sudo adduser <user_name>
```

***How to create a new group?***

```
sudo addgroup <group_name>
```

***How to add a user to a group?***

```
sudo usermod -aG <group_name> <user_name>
```

***How to change hostname?***

```
hostnamectl set-hostname <server_name>
```

Then connect to the server via ssh `ssh username@ipadress -p 4242`, you should see that the hostname has changed, but we still need to edit this file:

```
sudo nano /etc/hosts
```

And change the line with the former hostname to the new hostname. You can then reboot `sudo reboot` and the hostname should still be the new one.

***Where is sudo logs in /var/log/sudo?***

```
cd /var/log/sudo/00/00
ls
```

You will see a lot of directories with names like 01 2B 9S 4D etc. They contain the logs we need.

```
sudo apt update
ls
sudo echo hey
```

Now you see that we have a new directory here.

```
cd <nameofnewdirectory> && ls
```

***How to add and remove port 8080 in UFW?***

```
sudo ufw allow 8080 <- allow
sudo ufw status <- check
sudo ufw delete allow 8080 <- delete
```

***How to run script every 30 seconds?***

```
sudo crontab -e
```

Remove or commit previous cron "schedule" and add next lines in crontab file

```
*/1 * * * * /path/to/monitoring.sh
*/1 * * * * sleep 30s && /path/to/monitoring.sh
```

To stop script running on boot you just need to remove or commit

```
@reboot /path/to/monitoring.sh
```

line in crontab file.
