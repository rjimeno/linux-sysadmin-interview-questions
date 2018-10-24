Linux System Administrator/DevOps Interview Questions
====================================================

A collection of linux sysadmin/devops interview questions. Feel free to contribute via pull requests, issues or email messages.


## <a name='toc'>Table of Contents</a>

  1. [Contributors](#contributors)
  1. [General Questions](#general)
  1. [Simple Linux Questions](#simple)
  1. [Medium Linux Questions](#medium)
  1. [Hard Linux Questions](#hard)
  1. [Expert Linux Questions](#expert)
  1. [Networking Questions](#network)
  1. [MySQL Questions](#mysql)
  1. [DevOps Questions](#devop)
  1. [Fun Questions](#fun)
  1. [Demo Time](#demo)
  1. [Other Great References](#references)


#### [[⬆]](#toc) <a name='contributors'>Contributors:</a>

* [moregeek](https://github.com/moregeek)
* [typhonius](https://github.com/typhonius)
* [schumar](https://github.com/schumar)
* [negesti](https://github.com/negesti)
* peter
* [andreashappe](https://github.com/andreashappe)
* [quatrix](https://github.com/quatrix)
* [biyanisuraj](https://github.com/biyanisuraj)
* [pedroguima](https://github.com/pedroguima)
* Ben
* [bharatnc](https://github.com/bharatnc)


#### [[⬆]](#toc) <a name='general'>General Questions:</a>

* What did you learn yesterday/this week?
    * 2018-10-18: Simple way to "downgrade" Python 3.7 to 3.6 on my Mac:
    
    `$ brew switch python 3.6.5`


* Talk about your preferred development/administration environment. (OS,
Editor, Browsers, Tools etc.)

    * Development environment: Mac wih OS X & Emacs, closely followed by
        JetBrains IDEs.
    * Universal tool: Firefox or Crome web browsers. I still use Safari and
        Internet Explorer for specific purposes and testing.


* Tell me about the last major Linux project you finished.

    * TODO

    
* Tell me about the biggest mistake you've made in [some recent time period] and
    how you would do it differently today. What did you learn from this
    experience?
    
    * TODO

    
* Why we must choose you?
    * Because I'm eager to apply more of my knowledge to help Facebook users to
    stay connected with friends and family, to discover what's going on in the
    world, and to share and express what matters to them.
    (from the vision statement)

    
* What function does DNS play on a network?
    * The DNS translates domain names to the numerical IP addresses needed for
    locating and identifying computer services and devices with the underlying
    network protocols.
    * At its core, it translates more readily memorized domain names to the
    numerical IP addresses needed for locating and identifying computer services
    and devices with the underlying network protocols.
    * TODO: Elaborate on the advanced features.


* What is HTTP?
    * The Hypertext Transfer Protocol (HTTP) is an application protocol for
        distributed, collaborative, hypermedia information systems. HTTP is the
        foundation of data communication for the World Wide Web.

        
* What is an HTTP proxy and how does it work?

    * A proxy server is a server (a computer system or an application) that acts
        as an intermediary for requests from clients seeking resources from
        other servers. An HTTP proxy is Web proxy and uses the HTTP protocol.
        HTTP proxies can be used for multiple purposes including availability,
        reliability, anonymity, caching and more.

        
* Describe briefly how HTTPS works.
    * HTTPS encapsulates HTTP traffic into an SSL/TLS layer.

    
* What is SMTP? Give the basic scenario of how a mail message is delivered via
    SMTP.

    * A Simple Mail Transfer Protocol (SMTP) trivial example on how a message is
        delivered follows:
        
        1c. A SMTP client software resolves the name of the SMTP server it needs
            (based on DNS information) and establishes a TCP connection to port
            number 25.
            
        1s. The server shows it accepted the connection with a code 220 answer.
            
        2c. The client sends 'HELO ' followed by the server's domain name.
        
        2s. The server replies with a 250 "pleased to meet you" message,
            possibly describing the features it accepts.
            
        3c. The client sends 'MAIL FROM: ' followed by the email address of the
            sender.
            
        3s. The server normally replies with a 250 MAIL ok message.
        
        4c. The client sends 'RCPT TO: ' followed by the email address of the
            recipient.
            
        4s. The server sends a "250 ok" possibly repeating the recipient's
            email address as indicated above.
            
        5c. The client sends the 'DATA' command.
        
        5s. The server replies with '354' message indicating to proceed.
        
        6c. The client sends one or more lines of text that constitutes the
            email being sent. To indicate the end of the email data, the client
            sends a dot ('.') in a single line by itself.
            
        6s. The server replies with a 250 "message received" or "accepted" or
        "queued" for delivery.
        
        7c. The client sends the 'QUIT' command.
        
        7s. The server responds with a 221 "bye" message.


* What is RAID? What is RAID0, RAID1, RAID5, RAID10?

    * Is an array of (inexpensive or somewhat independent) disks working
        together to benefit from the cooperation. Some examples follow:
        
        * RAID0 allows for 2 or more disks join as a stripe set and behave as a
            stripe volume. At least two benefits can be obtained from striping:
            - Volumes can be larger than non-RAID volumes and,
            - Volumes can be faster thant non-RAID because data is split evenly
                between all participating disks.
                
        * RAID1 allows for multiple copies of a disk. Two are the key benefits:
            - Reliability as if disks in the array fail, the array keeps
                operating as long as there is still at least one disks that 
                works.
            - Performance is improved while reading as the data can be fetched
                from all the working copies.
                
        * RAID10 is also called RAID 1+0 and is a "nested" array that "mirrors"
            RAID1 stripes. A simple example would be mirrored pair of 3-disk
            stripes. The performance could be up to 6-time faster read 
            operations and 3-time faster write operations that can tolerate 
            the failure of 1, 2 or 3 disk as long as all the failures happen 
            on a single stripe. Note that a for RAID10 to keep operating, at 
            least one stripe must remain completely intact.
            
        * RAID5 is a standard (i.e. non-nested) array that keeps multiple copies
            of parity bits that permit the complete recovery of one of the disks
            in the array. RAID5 has low write performance compared to RAID0 &
            RAID1. On the other hand, RAID5 has the most efficient use of space.

            
* What is a level 0 backup? What is an incremental backup?
    * A level 0 backup is a "full backup". It is the first backup in a set of
        either incremental or differential set of backups.


* Describe the general file system hierarchy of a Linux system.
  * /bin/ = Essential User Command Binaries.
  * /boot/ = Static files required to boot the system, for example, the Linux
    kernel.
    These files are essential for the system to boot properly. 
  * /dev/ = Device nodes that represent devices attached to the system or
    virtual
    devices provided by the kernel. 
  * /etc/ = configuration files that are local to the machine (i.e.
    host-specific). It should not contain any binariesHost specific system 
    configuration.
  * /home/ = Data that only pertains to a specific user.
  * /media/ = Automatically detected removable media.
  * /mnt/ = Temporarily mounted file systems, such as NFS file system mounts.
  * /opt/ = Software and add-on applications packages that are not part of the
    default installation.
  * /proc/ = Special files that either extract information from the kernel or
    send information to it.
  * /sbin/ = System Binaries.
  * /srv/ = Site-specific data served. This directory gives users the location
    of data files for a particular service, such as FTP, WWW, or CVS. 
  * /tmp/ = Temporary Files.
  * /usr/ = Files that can be shared across multiple machines. Often a 
    partition that is mounted read-only. At a minimum, /usr/ should contain 
    the following subdirectories:
    * /usr/bin/ = Usef for binaries.
    * /usr/etc/ = System-wide configuration files.
    * /usr/games/ = Games?
    * /usr/include/ = C header files.
    * /usr/kerberos/ = Kerberos-related binaries and files.
    * /usr/lib/ = Object files and libraries that are not designed to be
      directly utilized by shell scripts or users.
    * /usr/libexec/ = Small helper programs called by other programs.
    * /usr/sbin/ = All system administration binaries, including those
      essential for booting, restoring, recovering, or repairing the system. 
      they require root privileges to use.
    * /usr/share/ = Store files that are not architecture-specific.
    * /usr/src/ = Source code.
    * /usr/tmp/ = Is linked to /var/tmp/ and stores temporary files.
    * /usr/local/ = Should be used to store software that should remain
      safe from system software upgrades.
  * /var/ = For variable data. Any program that write log files or need
    spool or lock directories should write them to the /var/ directory


#### [[⬆]](#toc) <a name='simple'>Simple Linux Questions:</a>

* What is the name and the UID of the administrator user?

  root, 0.
  
  
* How to list all files, including hidden ones, in a directory?

  `ls -a`
  
  
* What is the Unix/Linux command to remove a directory and its contents?

  `rmdir`
  
  
* Which command will show you free/used memory? Does free memory exist on Linux?

  `free`
  
  It does but it is called 'available' instead of 'free'. The core point here is
  that Linux will try to take advantage of all the installed memory. The memory
  that is not used by processes will be used for buffering and caches, but will
  immediately be made available if needed by for anything else, like running a
  process, for example.
  
  
* How to search for the string "my konfu is the best" in files of a directory
    recursively?
    
    `grep -r "my konfu is the best" <directory_name>`
    
    
* How to connect to a remote server or what is SSH?

    Secure Shell (SSH) is a cryptographic network protocol for operating network
    services securely over an unsecured network.
    
    A SSH client process can connect to a SSH server running in a remote machine.
    To open an interactive session the client software would be invoqued as:
    
    `ssh user12@system.example.com`
    
    where 'system.example.com' represents the name of the remote server and
    'user12' represents the name of the user that will be used to for log-in.
    

* How to get all environment variables and how can you use them?

    'set' should display all environment variables but it is probably beeter to
    use 'printenv' or 'env' instead, as only environment variables will be
    displayed.
    
    Environment variables can be used by writing and reading values to and from
    them as follows:
    
    `V=$(date)` # The variable V now holds the date-time at which it was assigned`
    
    The command above shows a way to set the variable V. The following one shows
    a way to read the value in V to display it:
    
    `echo $V # Displays the date and time when V was set using $(date)`


* I get "command not found" when I run ```ifconfig -a```. What can be wrong?

    On recent Linux distributions (like CentOS 7, for example), the net-tools package
    is not required and so, the command `ifconfig` may not be available. That is not
    necessarily wrong because the `ip` command can perform the same functionality.
    
    The specific functionality of `ifconfig -a` is the same (although not completely
    identical) as `ip link show`.


* What happens if I type TAB-TAB?

    The Bash shell will attempt to complete whichever command you are typing by
    "guessing" based on context.
    
    
* What command will show the available disk space on the Unix/Linux system?

    `df`
    

* What commands do you know that can be used to check DNS records?

    `dig` & `nslookup`
    
    
* What Unix/Linux commands will alter a files ownership, files permissions?

    `chown` & `chmod`
    
    
* What does ```chmod +x FILENAME``` do?

    Allows the file named FILENAME to be executed as a command, script or program.
    

* What does the permission 0750 on a file mean?

    The file's owner can read, write and execute the file, while the users that belog
    in the file's group can read and execute (thus, not write) the said file. Other
    users have no permissions at all on this file.
    
    
* What does the permission 0750 on a directory mean?

    That the directory's owner can read (as in `ls`), write (as in create, rename,
    and delete) files and attributes of the directory and enter (as in `cd`) the
    directory and access files and directories inside. Other users have no
    permissions whatsoever.
    

* How to add a new system user without login permissions?

    `useradd -s /sbin/nologin <username> -uid <uid>`
    
    In the command line above, `<username>` represents the username that the new
    system user will have while `<uid>` is a number between SYS_UID_MIN and
    SYS_UID_MAX that will identify this new user uniquely in this system. The
    values for SYS_UID_MIN and SYS_UID_MAX are often 200 and 999. They should be
    defined in the file `/etc/login.defs` and are often defined
    

* How to add/remove a group from a user?

    `useradd <username> -G <gid2>` can be used to create a new user with that will,
    additionally, belong to the group with id `<gid2>`. If the user already
    exists, its settings can be modified to add the group `<gid1>` from it as
    follows:
    
    `usermod -a -G <gid1> <username>`
    
    Finally if the user `<username>` already belongs to groups `<gid1>,<gid2>`,
    usrmod can be used to remove one or more of the additional groups as follows:
    
    `usermod -G <gid2> <username>`
    
    Where `<username>` will now belong only to the `<gid2>` group.

    
* What is a bash alias?

    `alias` is a Bash command that enables a replacement of a word by another
    string. It is mainly used to abbreviate typing. For example, the frequent
    command `git commit -m` can be shortened to something much shorter like `gsm`
    typing the following alias command:
    
    `alias gsm='git commit -m'`
    
    Users of DOS and the Windows operating system often alias the string `copy`
    to `cp` when using Unix-like operating system.
    
    
* How do you set the mail address of the root/a user?

    By editing root's entry in the `/etc/aliases` file and point it to the email
    address that will be used for root's email. Similarly, other local users can
    have their email forwarded to other email addresses by editing their entries
    on said file. After the file is changed, the program `newaliases` must be
    run. There are other ways to achieve a similar result like, for example, by
    using a `~/.forward` file.
    
    
* What does CTRL-c do?

    It causes the SIGINT signal to be sent to a process by its controlling
    terminal when a user wishes to interrupt its execution. 
    
    
* What is in /etc/services?

    A list of services including their names, the port and protocol
    combination they use additional names or aliases and comments.
    Effectively, the /etc/services is a database used by the
    C library routine getservbyname() to find the port number and
    protocol (TCP or UDP) used by a service given its name.
    
    
* How to redirect STDOUT and STDERR in bash? (> /dev/null 2>&1)

    In Bash's command line it is possible to redirect STDOUT to a file 
    named `output_file`, using `1> output_file` (or `> output_file` as the 
    number 1 that indicated STDOUT is optional). Similarly, `2> error_file` 
    redirects STDERR to the file `error_file`. Frequently, it is useful to 
    redirect STDERR not to a file but to STDOUT instead. To do that, `$1` can
     be used equivalently to STDOUT and, in that way, the redirection `2>&1` 
     will send STDERR to STDOUT.
     
     It is worth mentioning here that sometimes command or script should 
     produce absolutely no output to either STDOUT nor STDERR. One effective 
     way to achieve that is to follow the command with `> /dev/null 2>&1` as 
     that expression will send STDOUT to `/dev/null` and STDERR to STDOUT, 
     achieving in that way a completely quiet operation.
     


* What is the difference between UNIX and Linux.

    UNIX is a trademark that designates an operating system that
    certifiably adheres to the Singe UNIX Specification. Linux is
    the kernel of an operating system that behaves in a manner
    similar to a Unix system although does not certifiably conforms
    with the Single UNIX Specification.
    
    
* What is the difference between Telnet and SSH?

    * Simply put, both can be used to establish an interactive shell session 
    to a remote server. The key difference is that Telnet sends and receives 
    all its information in clear while, in contrast, the ssh client initiates
    by establishing secured communication with the server. In that way no 
    information is sent in clear. 


* Explain the three load averages and what do they indicate. What command can
  be used to view the load averages?
  
  * The `uptime` command (as well as others like `w` and `top`) can be used to
    view the load averages. They represent the average load calculated for the
    last 1, 5 & 15 minutes. In a system with multiple CPUs, TODO


* Can you name a lower-case letter that is not a valid option for GNU ```ls```?
* What is a Linux kernel module?
* Walk me through the steps in booting into single user mode to troubleshoot a problem.
* Walk me through the steps you'd take to troubleshoot a 404 error on a web application you administer.

#### [[⬆]](#toc) <a name='medium'>Medium Linux Questions:</a>

* What do the following commands do and how would you use them?
 * ```tee```
 * ```awk```
 * ```tr```
 * ```cut```
 * ```tac```
 * ```curl```
 * ```wget```
 * ```watch```
 * ```head```
 * ```tail```
* What does an ```&``` after a command do?
* What does ```& disown``` after a command do?
* What is a packet filter and how does it work?
* What is Virtual Memory?
* What is swap and what is it used for?
* What is an A record, an NS record, a PTR record, a CNAME record, an MX record?
* Are there any other RRs and what are they used for?
* What is a Split-Horizon DNS?
* What is the sticky bit?
* What does the immutable bit do to a file?
* What is the difference between hardlinks and symlinks? What happens when you remove the source to a symlink/hardlink?
* What is an inode and what fields are stored in an inode?
* How to force/trigger a file system check on next reboot?
* What is SNMP and what is it used for?
* What is a runlevel and how to get the current runlevel?
* What is SSH port forwarding?
* What is the difference between local and remote port forwarding?
* What are the steps to add a user to a system without using useradd/adduser?
* What is MAJOR and MINOR numbers of special files?
* Describe the mknod command and when you'd use it.
* Describe a scenario when you get a "filesystem is full" error, but 'df' shows there is free space.
* Describe a scenario when deleting a file, but 'df' not showing the space being freed.
* Describe how 'ps' works.
* What happens to a child process that dies and has no parent process to wait for it and what’s bad about this?
* Explain briefly each one of the process states.
* How to know which process listens on a specific port?
* What is a zombie process and what could be the cause of it?
* You run a bash script and you want to see its output on your terminal and save it to a file at the same time. How could you do it?
* Explain what echo "1" > /proc/sys/net/ipv4/ip_forward does.
* Describe briefly the steps you need to take in order to create and install a valid certificate for the site https://foo.example.com.
* Can you have several HTTPS virtual hosts sharing the same IP?
* What is a wildcard certificate?
* Which Linux file types do you know?
* What is the difference between a process and a thread? And parent and child processes after a fork system call?
* What is the difference between exec and fork?
* What is "nohup" used for?
* What is the difference between these two commands?
 * ```myvar=hello```
 * ```export myvar=hello```
* How many NTP servers would you configure in your local ntp.conf?
* What does the column 'reach' mean in ```ntpq -p``` output?
* You need to upgrade kernel at 100-1000 servers, how you would do this?
* How can you get Host, Channel, ID, LUN of SCSI disk?
* How can you limit process memory usage?
* What is bash quick substitution/caret replace(^x^y)?
* Do you know of any alternative shells? If so, have you used any?
* What is a tarpipe (or, how would you go about copying everything, including hardlinks and special files, from one server to another)?
* How can you tell if the httpd package was already installed?
* How can you list the contents of a package?
* How can you determine which package is better: openssh-server-5.3p1-118.1.el6_8.x86_64 or openssh-server-6.6p1-1.el6.x86_64 ?
* Can you explain to me the difference between block based, and object based storage?

#### [[⬆]](#toc) <a name='hard'>Hard Linux Questions:</a>

* What is a tunnel and how you can bypass a http proxy?
* What is the difference between IDS and IPS?
* What shortcuts do you use on a regular basis?
* What is the Linux Standard Base?
* What is an atomic operation?
* Your freshly configured http server is not running after a restart, what can you do?
* What kind of keys are in ~/.ssh/authorized_keys and what it is this file used for?
* I've added my public ssh key into authorized_keys but I'm still getting a password prompt, what can be wrong?
* Did you ever create RPM's, DEB's or solaris pkg's?
* What does ```:(){ :|:& };:``` do on your system?
* How do you catch a Linux signal on a script?
* Can you catch a SIGKILL?
* What's happening when the Linux kernel is starting the OOM killer and how does it choose which process to kill first?
* Describe the linux boot process with as much detail as possible, starting from when the system is powered on and ending when you get a prompt.
* What's a chroot jail?
* When trying to umount a directory it says it's busy, how to find out which PID holds the directory?
* What's LD_PRELOAD and when it's used?
* You ran a binary and nothing happened. How would you debug this?
* What are cgroups? Can you specify a scenario where you could use them?
* How can you remove/delete a file with file-name consisting of only non-printable/non-type-able characters?
* How can you increase or decrease the priority of a process in Linux?
* What are run-levels in Linux?


#### [[⬆]](#toc) <a name='expert'>Expert Linux Questions:</a>

* A running process gets ```EAGAIN: Resource temporarily unavailable``` on reading a socket. How can you close this bad socket/file descriptor without killing the process?
* What do you control with swapiness?
* How do you change TCP stack buffers? How do you calculate it?
* What is Huge Tables? Why isn't it enabled by default? Why and when use it?
* What is LUKS? How to use it?


#### [[⬆]](#toc) <a name='network'>Networking Questions:</a>

* What is localhost and why would ```ping localhost``` fail?
* What is the similarity between "ping" & "traceroute" ? How is traceroute able to find the hops.
* What is the command used to show all open ports and/or socket connections on a machine?
* Is 300.168.0.123 a valid IPv4 address?
* Which IP ranges/subnets are "private" or "non-routable" (RFC 1918)?
* What is a VLAN?
* What is ARP and what is it used for?
* What is the difference between TCP and UDP?
* What is the purpose of a default gateway?
* What is command used to show the routing table on a Linux box?
* A TCP connection on a network can be uniquely defined by 4 things. What are those things?
* When a client running a web browser connects to a web server, what is the source port and what is the destination port of the connection?
* How do you add an IPv6 address to a specific interface?
* You have added an IPv4 and IPv6 address to interface eth0. A ping to the v4 address is working but a ping to the v6 address gives you the response ```sendmsg: operation not permitted```. What could be wrong?
* What is SNAT and when should it be used?
* Explain how could you ssh login into a Linux system that DROPs all new incoming packets using a SSH tunnel.
* How do you stop a DDoS attack?
* How can you see content of an ip packet?
* What is IPoAC (RFC 1149)?
* What will happen when you bind port 0?



#### [[⬆]](#toc) <a name='mysql'>MySQL questions:</a>

* How do you create a user?
* How do you provide privileges to a user?
* What is the difference between a "left" and a "right" join?
* Explain briefly the differences between InnoDB and MyISAM.
* Describe briefly the steps you need to follow in order to create a simple master/slave cluster.
* Why should you run "mysql_secure_installation" after installing MySQL?
* How do you check which jobs are running?
* How would you take a backup of a MySQL database?

#### [[⬆]](#toc) <a name='devop'>DevOps Questions:</a>

* Can you describe your workflow when you create a script?
* What is GIT?
* What is a dynamically/statically linked file?
* What does "./configure && make && make install" do?
* What is puppet/chef/ansible used for?
* What is Nagios/Zenoss/NewRelic used for?
* What is Jenkins/TeamCity/GoCI used for?
* What is the difference between Containers and VMs?
* How do you create a new postgres user?
* What is a virtual IP address? What is a cluster?
* How do you print all strings of printable characters present in a file?
* How do you find shared library dependencies?
* What is Automake and Autoconf?
* ./configure shows an error that libfoobar is missing on your system, how could you fix this, what could be wrong?
* What are the advantages/disadvantages of script vs compiled program?
* What's the relationship between continuous delivery and DevOps?
* What are the important aspects of a system of continuous integration and deployment?
* How would you enable network file sharing within AWS that would allow EC2 instances in multiple availability zones to share data?

#### [[⬆]](#toc) <a name='fun'>Fun Questions:</a>

* A careless sysadmin executes the following command: ```chmod 444 /bin/chmod ``` - what do you do to fix this?
* I've lost my root password, what can I do?
* I've rebooted a remote server but after 10 minutes I'm still not able to ssh into it, what can be wrong?
* If you were stuck on a desert island with only 5 command-line utilities, which would you choose?
* You come across a random computer and it appears to be a command console for the universe. What is the first thing you type?
* Tell me about a creative way that you've used SSH?
* You have deleted by error a running script, what could you do to restore it?
* What will happen on 19 January 2038?
* How to reboot server when reboot command is not responding?


#### [[⬆]](#toc) <a name='demo'>Demo Time:</a>

* Unpack test.tar.gz without man pages or google.
* Remove all "*.pyc" files from testdir recursively?
* Search for "my konfu is the best" in all *.py files.
* Replace the occurrence of "my konfu is the best" with "I'm a linux jedi master" in all *.txt files.
* Test if port 443 on a machine with IP address X.X.X.X is reachable.
* Get http://myinternal.webserver.local/test.html via telnet.
* How to send an email without a mail client, just on the command line?
* Write a ```get_prim``` method in python/perl/bash/pseudo.
* Find all files which have been accessed within the last 30 days.
* Explain the following command ```(date ; ps -ef | awk '{print $1}' | sort | uniq | wc -l ) >> Activity.log```
* Write a script to list all the differences between two directories.
* In a log file with contents as ```<TIME> : [MESSAGE] : [ERROR_NO] - Human readable text``` display summary/count of specific error numbers that occurred every hour or a specific hour.


#### [[⬆]](#toc) <a name='references'>Other Great References:</a>

Some questions are 'borrowed' from other great references like:

* https://github.com/darcyclarke/Front-end-Developer-Interview-Questions
* https://github.com/kylejohnson/linux-sysadmin-interview-questions/blob/master/test.md
* http://slideshare.net/kavyasri790693/linux-admin-interview-questions
