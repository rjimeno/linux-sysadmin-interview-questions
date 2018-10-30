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
    redirect STDERR not to a file but to STDOUT instead. To do that, `&1` can
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
    last 1, 5 & 15 minutes.
     
    The load (more accurately System Load or CPU Load) indicates system
    utilization and represents the number of processes in the running or
    runnable (or uninterruptible sleep, in the case of Linux) state at a given
    time. Observe that a 1-core CPU system load of 1 represents 100% utilization
    while the same load on a 4-core CPU system load represents only 25%
    utilization.


* Can you name a lower-case letter that is not a valid option for GNU ```ls```?

    * Only e, j, y & z. In at least one BSD (MacOS), e is used to display 
      access control lists, but the others also absent there. 
    

* What is a Linux kernel module?

    Is a piece of code that extends the functionality of kernel without the 
    need to rebuild nor reboot the system. Loadable kernel modules can be 
    loaded-to and unloaded-from the kernel as needed. In Linux many device 
    drivers are modules. Because of that, device drivers of devices that are 
    not used, can be removed (or never loaded) without rebooting.
    

* Walk me through the steps in booting into single user mode to troubleshoot a
  problem.

    * On a RHEL7 that is responsive: `systemctl isolate runlevel1.target`.
    
    * On some other Linux: `telinit 1` (or `init 1` or `runlevel 1`).
    
    * On a non-responsive (halted or crashed) system:
    
        * Start rebooting and when the system starts the boot loader, type 
        something to stop the process for continuing. Edit the kernel line 
        (the one that starts with 'kernel') and append ' single ' to it. Then
        send a Ctrl-X to continue the boot process to runlevel 1.
         
    * On a RHEL7 that is non-responsive:
    
        * Do similarly the case above but instead of editing the line that 
        starts with kernel, edit the line that starts with 'linux16'. Do not 
        append ' single '. Instead, replace the ' ro ' in that line for ' rw 
        init=/sysroot/sh ' and send Ctrl-X to continue rebooting to rescue mode.
        
        * Once the boot process stops and offers a prompt, issue the command 
        `chroot /sysroot/` to mount get the root file system setup as it 
        usually does in runlevel 1 or single user mode.

    
* Walk me through the steps you'd take to troubleshoot a 404 error on a web 
application you administer.

    * I'd try to obtain the URL(s) that is(are) triggering the error. That's 
    a good starting poing because, from there I can try to identify if there 
    was an obvious typo in the URL, etc. If that's not the problem ...
    
    * I'd try to identify the time at which the 404 happened and check the 
    errors.log file to try spotting the problem or problem's there. Maybe 
    just by glancing a the 404s there I can see a pattern in the problem.
    
    * After that, I'd check httpd.conf and try to "cross reference" the
    error(s) with the configuration. For example, maybe I can identify that 
    all the 404 errors correspond to a single branch (or even file) in the 
    file system hierarchy. If that is the case, the problem could be related 
    to a recent change in the permissions of directories or files. This kind 
    of problem may happen not only after an update on a web site, but also 
    after recovering a backup.
    
    * If the problem does not seem to be associated with files, maybe the 
    problem is related to DNS or IP addresses in virtual host configurations.
    For example, maybe the errors come from a web site with a domain name 
    that expired recently. The way to solve that problem may be completely 
    outside of the web server scope and be dealt with the person responsible 
    of timely paying for domain names.


#### [[⬆]](#toc) <a name='medium'>Medium Linux Questions:</a>

* What do the following commands do and how would you use them?
 * ```tee```
 
    * Sends the standard input to standard output *AND* a file. Useful to be 
    able to see the output of a script as it happens while keeping a 
    persistent copy of everything at the same time.
 
 
 * ```awk```
 
    * Is an interpreted programming language designed for text processing and
     typically used as a data extraction and reporting tool. I'd use it to 
     process column-oriented plain-text files to create reports with 
     consolidated data.
    
   
 * ```tr```
 
    * Translates or transliterates its input based on a couple of strings 
    that help match an ordered set of characters to another one. Id use it to
     "clean" data files that contain some information tha is not relevant for
      analysis and that could make the processing of the input data more 
      difficult.
    
    
 * ```cut```
 
    * Selects sub-sections of line-oriented data using column-oriented 
    information to process input files and produce relevant information. In a
     way `cut` is "just" a filter, but its capacity to sub-select data in
    flexible ways makes it a great tool.
 
 
 * ```tac```
 
    * Concatenates the content of the files provided as arguments, and 
    reversed the output. It is similar to the cat command, but displays the 
    output in the opposite order. It is useful to review and see log files 
    showing the oldest entries first instead of last (as cat would do).
 
 
 * ```curl```
 
    * Curl is a tool to transfer data from or to a remote networked server 
    using protocols like FTP and HTTP. It is useful for testing APIs over 
    HTTP and much, much, much more.
    
    
 * ```wget```
 
    * Wget is a utility for non-interactive download of files from the Web 
    using FTP, HTTP or HTTPS. I'd use it to copy static web sites to my 
    laptop so I can review the downloaded information while offline and using
    software tools that would not normally be available for the web.
 
 
 * ```watch```
 
    * Executes commands at specified intervals. I'd use it to monitor the 
    operation of other programs using, for example, ps as follows:
    
    `watch "ps -e"`
    
    A strong point for using watch is the way it keeps information on screen.
    
 
 
 * ```head```

    * Shows the top few lines of a data file. Can be used to see the most 
    recent entries in a log file
    
    
 * ```tail```
 
    * Shows the bottom few lines of a data file. Can be used to see the oldest
    entries in a log file.
 
 
* What does an ```&``` after a command do?

    * It executes the command "in the background", which means the shell does
      not wait for the command to finish and instead it executes it in a
      separate shell (using 0 as its return status). It is useful when we can
      safely ignore the return status of the command and can benefit from not
      having to wait for the command to finish execution and continue typing new
      commands.
    
    
* What does ```& disown``` after a command do?

    * Removes a background process from the shell's job control while leaving it
      connected to the terminal. It is useful when we want to prevent the shell
      from sending the HUP signal (SIGHUP) to the command.q


* What is a packet filter and how does it work?

    * A packet filter is a software tool that helps at controlling access to 
    a computer network. It works by analyzing the TCP/IP information on 
    packets requesting pass-through and permitting, or not, their flow. 


* What is Virtual Memory?

    * Virtual memory is a memory management capability of an OS that allows a
      computer to compensate for physical memory shortages by temporarily
      transferring data from random access memory to persistent storage.


* What is swap and what is it used for?

    * To swap is the process of writing memory (that is RAM) pages to persistent
     storage and reading data from into memory. Swapping requires swap space 
     in the form of either a swap file or a swap partition (or volume).


* What is an A record, an NS record, a PTR record, a CNAME record, an MX record?

    * An A record maps a FQDN to one IP addresses.
    
    * PTR records are the "complement" of A records in the sense that they 
    map IP addresses to FQDN names. They have the numbers in the IP address 
    reversed and appended with in-addr.arpa. Email servers often reject email
    from sources with unmatched PTR to A records.
    
    * CNAME records associate additional names to canonical names 
    effectively creating aliases.
    
    * An MX record specifies a mail server responsible for accepting email 
    messages on behalf oa a recipient's domain along with a "priority" when 
    redundant servers are available.
    

* Are there any other RRs and what are they used for?

    * SOA (Start Of Authority) records specify authoritative information on a
     DNS zone.

    * NS records indicate which name server(s) are authoritative for the zone.
    
    * TXT records were created for human readable text (like comments, for 
    example) but nowadays are used also for multiple purposes including 
    "machine-readable" text.
    
    * SRV are generalized service location records that can be used for newly
     created services.
     

* What is a Split-Horizon DNS?

    * Is the facility of a DNS implementation to provide different sets of DNS
      information depending on information provided by the client (and usually
      being the source address of the DNS request) For example, By using
      split-horizon DNS the same name can lead to either the private IP address
      or the public one, depending on which client sends the query.
    

* What is the sticky bit?

    * Is metadata (from regular Unix permissions) that indicates a directory 
    should be given special treatment as follows:
    
    A directory with the sticky bit set forbids users from deleting or 
    renaming a file owned by other user.
    

* What does the immutable bit do to a file?

    * It prevents a file from being linked (that is, hard-linked, not 
    soft-linked), renamed, deleted or modified in any way, except for root. 
    It also helps root from accidentally doing so.
    
    
* What is the difference between hardlinks and symlinks? What happens when 
you remove the source to a symlink/hardlink?

    * Files contain data and have associated metadata, like their names, for 
    example. Links are additional names for files that facilitate access to 
    to files using different names. Links come in two types: Hard links and 
    symbolic links. Symbolic links are implemented as independent or 
    additional file that contain the name of the linked file along with 
    metadata indicating that the file has type "symlink" (as oposed of 
    directories or devices). Note that symbolic links can link files in 
    separate file systems. Note too that if the linked file is deleted, the 
    symbolic link is effectively linked to nothing. Hard links are 
    implemented differently and do not suffer from the formerly described 
    deletion problem: if one of the names linking to the file is deleted, the
     link still points to the file. On the other hand hard links can't 
     associate files in separate file systems: both must belong in the same 
     file system.

* What is an inode and what fields are stored in an inode?

    * An inode is a data structure of Unix-like file systems that contains 
    metadata and pointers to storage blocks (containing data) and other 
    inodes. It is safe to think of inodes as smart building blocks of files.
    
    * Inodes contain fields like the following:
        * Device ID identifies uniquely the device that contains the file 
        represented with this inode.
        * File mode which determines the file type and the way in which the 
        file can be accessed by the owner, its group & others.
        * A (hard) link count.
        * UID & GID for this file.
        * Device ID of the file if this file represents a device file.
        * File size in bytes.
        * Timestamps for last modification of metadata (i.e. for the inode 
        itself), last modification of the file content and last access time 
        (ctime, mtime & atime).
        * Prefered I/O block size.
        * The number of blocks allocated to this file.
        * Direct, "singly", "doubly" and "triply" indirect pointers for data 
        blocks.
         

* How to force/trigger a file system check on next reboot?

    * `touch /forcefsck` will trigger a file system check on the next reboot 
    for the root file system.
    
    * Observe that this mechanism is not necessary for non-root file systems 
    as they can be dismounted to perform a file system check.
    
    
* What is SNMP and what is it used for?

    * It is the Simple Network Management Protocol; an Internet Starndard, 
    application-level protocol for managing network devices as well as 
    collection and organizing information about a network and its components.

* What is a runlevel and how to get the current runlevel?

    * A runlevel is a mode of operation in Unix-like operating systems that 
    implement a System V-style initialization. A runlevel can be thought as a
     set of functionality that is enabled at a point in time for an operating
      system (running) instance, or the state of a machine after boot. 
      Usually, 7 runlevels existe with runlevel numbers 0 & 6 being a bit 
      special in the representing halting and rebooting a system. Runlevel 1 
    is often defined as having minimal capabilities and useful for a single 
    user for maintenance or troubleshooting operations. Those are the 
    standard runlevels. Additionally, runlevel 3 
    includes fully operational network connectivity for multiple users and 
    runlevel 5 has all the features of runlevel 3 plus a graphical user 
    interface for computers capable of using X11. Runlevels vary 
    significantly from with versions and vendors; even more the nonstandard 
    (1 to 5) runlevels.
    
    * The current runlevel can be queried by running the command `runlevel`. 
    The output includes the current runlevel. `runlevel` seem to be available
     even on recent Linux distributions that are replacing the concept of 
     runlevels and the init process by targets and systemd.


* What is SSH port forwarding?

    * SSH port forwarding is SSH tunneling. an SSH tunnel establishes a 
    ciphered channel of communication between two ports of one or two 
    networked servers. It is useful for securing communication that otherwise
     would be send or received in-clear. TODO


* What is the difference between local and remote port forwarding?

    * TODO
    
    
* What are the steps to add a user to a system without using useradd/adduser?

    * As root:
        * Create entries in /etc/passwd and /etc/shadow for the new user.
            * You will probably need to use vipw to edit those files.
            * To create the entries, a number of small decision like choosing
             a correct UID and identifying if this user actually needs an 
             interactive shell (maybe /usr/sbin/nologin is best).
        * If the user will have a home directory, create it by copying 
        /etc/skel/.
        * If the user will need to authenticate to the system, assign a 
        password for by invoking `passwd username`. Note that you might need 
        a good way (secure and efficient) way to communicate the password to 
        the new user.
        
        
* What is MAJOR and MINOR numbers of special files?

    * The files under /dev/ are not regular files. They represent devices and
     some other things  - like a random number generator /dev/random, for 
     example -  communicate with the kernel through a device driver.
     
     The specific device driver for each device is identified by a number, 
     and that is the MAJOR number. Often times multiple devices are operated 
     by the same device driver and the device driver needs a way to identify 
     each one of the individual devices that share the same device driver. 
     That number is the MINOR number.


* Describe the mknod command and when you'd use it.

    * Mknod can create the special (device) files described in the previous 
    question.
    

* Describe a scenario when you get a "filesystem is full" error, but 'df' shows there is free space.

    * When a very large number of (possibly very small) files have consumed 
    all the inodes for that file system instance.
    

* Describe a scenario when deleting a file, but 'df' not showing the space 
being freed.

    * Say a file is opened by a process and immediately deleted (or 
    "unlinked"). Even though the link count in the inode is now zero and the 
    file can't be reached from the file system hierarchy (i.e. it has been 
    deleted for most purposes), the process still has a file descriptor open 
    and pointing to the file. So, the space occupied by the file can't be 
    released as available storage space until the file close() is called for 
    the open descriptor.


* Describe how 'ps' works.

    * On Linux, the /proc/ psudo-filesystem hierarchy contains extensive 
    information on the system's processes. All the information required for 
    `ps` is there although I, personally, do not know what exactly would need
     to be checked and what can be ignored for `ps`. Also, I'm confident in 
     thinking that there must be one or more libraries that simplify the 
     querying of /proc/. `man 5 proc` is probably a great starting point.
      

* What happens to a child process that dies and has no parent process to wait
 for it and what’s bad about this?
 
    * If the parent process does not call wait(), the child stays in the 
    zombie state ocupying an entry in the process table. If the number of 
    zombie processes keeps increasing, the system runs out of PDIs (or 
    entries in the process table) and becomes stalled.
    

* Explain briefly each one of the process states.

    * Running : The process is either running or it is ready to run .
    * Waiting : The process is waiting for an event or for a resource.
    * Stopped : The process has been stopped, usually by receiving a signal.
    * Zombie : The process is dead but have not been removed from the process
     table.
    TODO: Improve on the above, possible with information from `man ps` as:
                     D    uninterruptible sleep (usually IO)
                     R    running or runnable (on run queue)
                     S    interruptible sleep (waiting for an event to complete)
                     T    stopped by job control signal
                     t    stopped by debugger during the tracing
                     W    paging (not valid since the 2.6.xx kernel)
                     X    dead (should never be seen)
                     Z    defunct ("zombie") process, terminated but not reaped by its parent

* How to know which process listens on a specific port?

    * For example, say we want to find out which process listens to port 80 
    using protocol TCP. I would:
    
        * Preferably use `lsof -i TCP:80`
        
    Until recently, I'd have used `netstat -tulpn | grep tcp | grep :80`, but 
    netstat is nnot installed by default on systems like RHEL 7 (and so, 
    CentOS 7). I learned that linux also has `fuser 80/tcp`. 

    
* What is a zombie process and what could be the cause of it?

    * It is a process that has diet but its parent process yas not yet called
     wait() on it to collect the exit code left in the process table.
     
    * If the parent process is not written carefully, a bug may prevent it 
    from calling wait() correctly.
    
    
* You run a bash script and you want to see its output on your terminal and 
save it to a file at the same time. How could you do it?

    * `./bash_script | tee file_name`
    
    The above command will copy its standard input to its standard output and
     to a file called 'file_name'.


* Explain what echo "1" > /proc/sys/net/ipv4/ip_forward does.

    * Would enable the IP Forwarding feature of the TCP/IP stack in the 
    kernel. When Linux is used for routing or firewalling this feature should
    be enabled.  


* Describe briefly the steps you need to take in order to create and install 
a valid certificate for the site https://foo.example.com.

    * TODO


* Can you have several HTTPS virtual hosts sharing the same IP?

    * TODO
    
    
* What is a wildcard certificate?

    * TODO
    
    
* Which Linux file types do you know?

    This question is a bit ambiguous or unclear to me. I'm choosing to answer it
    in the following way:
    
    * There are at least two groups of file types: Special files and regular
    files. Here are the file types I know of:
    
        * Special files can be directories, links, pipes, sockets and device 
        files (block and character). `find -type` can be useful on this regard
        
        * Regular files can have different formats: executable files in a 
        binary format like a.out or ELF, executable shell commands text, PDF 
        documents, PNG image data and more. The last two examples are 
        non-executable. The `file` command can be useful on this regard.
        
        
* What is the difference between a process and a thread? And parent and child
 processes after a fork system call?
 
    * Processes have separate and independent memory. A single process can 
    have multiple threads and those share memory between them. Besides that 
    very important difference, processes and threads are quite similar in Linux.
    

* What is the difference between exec and fork?

    * While exec() and fork() are often used together, they are quite 
    different. exec() replaces the current process image with a new process 
    image. fork() creates a new and exact copy of the current process. Often,
     programs call fork() and determine if the current process is the parent 
     or a child. Then, the child calls exec().


* What is "nohup" used for?

    * Sometimes we need to run a process that will take a long time to
    finish. Long time in this case means longer than the session may last. 
    Nohup "deattaches" from the session (or terminal) a process that runs in 
    the background. The effective result of this is that the session can be 
    closed and the program will continue running until it finishes its 
    execution normally. Also, the output will be kept in a file (named
    nohup.out by default) in case it needs to be checked at a later time.



* What is the difference between these two commands?
 * ```myvar=hello```
 * ```export myvar=hello```
 
    * Without `export`, only the current process will have that variable's 
    value. If sub-shells (children processes, to be a bit more accurate) will
     need the value, then the variable must be exported.
     
     
* How many NTP servers would you configure in your local ntp.conf?

    * Four is the recommended minimum.
    
    
* What does the column 'reach' mean in ```ntpq -p``` output?

    It represents the status of the last 8 NTP transactions between the NTP 
    daemon and a given remote time server. Observe that that the number 
    appears on base 8 (octal), which could be confusing. The right-most bit 
    represents the most recent transaction and the left-most bit represents 
    the oldest transaction that's tracked. Zero means failure vs one 
    for success. 
    
    

* You need to upgrade kernel at 100-1000 servers, how you would do this?

    * I'll divide the answer in two parts:
    
        * At the server level, the command(s) `yum -y update kernel & reboot`
        must be executed by a user with root privileges. That can be achieved
        by using a scheduled job (via cron or similar). Other option is to 
        generate an SSH key pair on a "controller" server and install the 
        public key on all of the 100-1000 other servers, then the 
        controller server would be able run a simple script to read the host 
        names from a file and execute the command remotely on all servers. 
        Configuration management software like Ansible, Chef & Puppet may be 
        able to achieve this too.
        
        * Above the server level there is the problem of coordinating the 
        upgrades: In most cases, you rather not have all those servers 
        upgrade their kernels and reboot at approximately the same time, but 
        instead in piecemeal controlled groups. Another problem may be about 
        wasting network bandwidth or time. Copying the relevant .rpm files to
        a on-premises repository or shared disk are possible solutions.


* How can you get Host, Channel, ID, LUN of SCSI disk?

    * By visually inspecting (skimming & scanning) the output of the 
    following 3 commands:
    
    `cat /proc/scsi/scsi` the 'Host' line or lines are the most relevant.
    
    `ls -ld /sys/block/sd*/device` should link to device files with names 
    that end their names with the numbers for "host:channel:id:lun".
    
    `ls -la /dev/disk/by-id/` will point to actual ("short") device names.
     
    
* How can you limit process memory usage?

    * `ulimit -Sv` followed by the maximum number of KB that the future 
    processes will be allowed to use.
    

* What is bash quick substitution/caret replace(^x^y)?

    *It is a way to (almost) repeat the previous command replacing the first 
    instance of the string 'x' by the string 'y'. Example
    
    ```
    $ echo baz foo foo
    baz foo foo
    $ ^foo^bar
     echo baz bar foo
    baz bar foo
    $
    ```
    
* Do you know of any alternative shells? If so, have you used any?

    * I used csh a few years MANY years ago and I'm happier with Bash nowadays. 
    There are many other shells like sh, ksh, tcsh, and more.
    
    
* What is a tarpipe (or, how would you go about copying everything, including
 hardlinks and special files, from one server to another)?

    * Many years ago I had only one server with a tape device and so I used 
    telnet, tar and pipes to initiate the creation of a backup that will be 
    received by the server with tape capabilities and recorded there. I 
    learned the trick from the book Unix Power Tools (probably first edition).
    
    *  A quick Google search showed ways to do similar things using ssh so a 
    whole file system can be backed up to a remote host. Here's an example:
    
    `tar zcf - tobearchived | ssh user@destination_server_ip 'cat - > tobearchived.tar.gz'`
 
    'tobearchived' represents a file or, more interestingly, hierarchy of 
    files or full file system in a (origin) server. 'user' is not very 
    relevant, but it is necessary while 'destination_server_ip' is the domain
     name or IP address of the host that will receive the stream of data to 
     be archived as a tape archive file.
     
 
* How can you tell if the httpd package was already installed?

    * My preferred way is to try calling `apachectl`. It is probably better 
    to query the package manager considering that the name of the package is 
    varies between distributions and their versions. You will probably need 
    to "grep" the output for 'http' or '[Aa]pache'.
    
    
* How can you list the contents of a package?

    `rpm -ql <package_name>` if the package is installed. It is `rpm -qlf 
    <package_file>` works if the package is not installed but its file is 
    available in the local file system. Yum and apt-get can do similar things.
    

* How can you determine which package is better: openssh-server-5.3p1-118.1
.el6_8.x86_64 or openssh-server-6.6p1-1.el6.x86_64 ?

    * Generally, higher numbers towards the left represent are equivalent to 
    more recent packages and so it may be OK to assume that openssh-server-6
    .6p1-1.el6.x86_64 is better (Major version 6 as oposed to version 5).


* Can you explain to me the difference between block based, and object based 
storage?

    * The following is an oversimplification:
    
        * Block based storage is fast and can have a file system on top. The 
        way it works allow for a program to append one or more bytes at the 
        end of a large file very quickly.
        
        * Object storage is comparatively slow. It is not possible to add a 
        byte at the end of a file without retrieving the entirety of the file 
        first.

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

    * One possibility is: the local host interface (lo) is down. To fix that,
     try: `ip link set lo up`.
     
    * Another posibility is: The TCP/IP stack is ignoring all ICMP Echo 
    requests. To fix it, try: `echo "0" > 
    /proc/sys/net/ipv4/icmp_echo_ignore_all`
    
* What is the similarity between "ping" & "traceroute" ? How is traceroute 
able to find the hops.

    * Both Ping and Traceroute utilities use ICMP for their purposes. 
    Traceroute controls the Time To Live (TTL) or hop-pimit value in a ICMP 
    datagram and looks for for time-exceeded-in-transit and 
    destination-unreachable responses, to identify gateways on a path.
    
    * I vaguely remember that Traceroute also uses the "record route" feature
     of IP to construct its response, but I can't recall enough details. 


* What is the command used to show all open ports and/or socket connections 
on a machine?

    `netstat -tulpn` or equivalently `ss -lpn`.
    

* Is 300.168.0.123 a valid IPv4 address?

    * No: The left-most number can't be represented by an 8-bit byte.


* Which IP ranges/subnets are "private" or "non-routable" (RFC 1918)?

    * 10.0.0.0 / 8 (i.e., to 10.255.255.255)
    * 172.16.0.0 / 12 (i.e., to 172.31.255.255)
    * 192.168.0.0 / 16 (i.e., to 192.168.255.255)
    
    
* What is a VLAN?

    * It is a Virtual Local Area Network. A VLAN grpups devices in a 
    broadcast domain (logical grouping, that is; as opposed to physical 
    grouping). VLANs can be used to improve congestion, scalability and 
    security while simplifying network management and, to some extent, 
    network architecture design.
    

* What is ARP and what is it used for?

    Address Resolution Protocol. It is used to map or associate addresses in 
    the Media Access Control (MAC) or Logical Link layer to IP addresses in 
    the Network layer.
    

* What is the difference between TCP and UDP?

    * UDP is a simple, high-speed, low-functionality protocol that interface
    applications to the network layer. In contrast, TCP is a possibly slower,
    fully-featured, reliable protocol that isolates applications from common 
    problems at the network layer.
    
    * UDP is connection-less, while TCP is connection-oriented.
    
    * UDP is message-based while TCP is stream-based.
    
    * UDP is inreliable  while TCP is reliable.
    
    * UDP does not retransmit on its own while TCP takes care of 
    retransmissions when needed.
    
    * UDP does not manage the flow of data while TCP uses sliding 
    windows heuristics and congestion control avoidance algorithms.
    
    * UDP is very lean with a extremely low overhead. TCP is still lean with 
    low overhead but not as much as UDP.
    
    * UDP has very high "raw" transmission speed. TCP uses its advanced 
    features to provide hight transmission speed even under adverse 
    circumstances.
    
    * UDP is ideal for small to moderate amounts of data while TCP scales 
    efficiently up to very large amounts of data.


* What is the purpose of a default gateway?

    * Its purpose is to forward packets from a network when no other route 
    matches.


* What is command used to show the routing table on a Linux box?

    `route` or `ip route`.


* A TCP connection on a network can be uniquely defined by 4 things. What are
 those things?

    * Source address, source port, destination address, and destination port 
    numbers.
    

* When a client running a web browser connects to a web server, what is the 
source port and what is the destination port of the connection?

    * Source port is unknown; it is an ephemeral port larger than 1023 
    assigned arbitrarily. 
    
    * Destination port should be 80 although, in trying to be accurate, 80 is
     the default port for a web server but its using a different port number 
     would not prevent it from still being a web server.
     

* How do you add an IPv6 address to a specific interface?

    * `/sbin/ip -6 addr add <ipv6address>/<prefixlength> dev <interface>`


* You have added an IPv4 and IPv6 address to interface eth0. A ping to the v4
 address is working but a ping to the v6 address gives you the response
 ```sendmsg: operation not permitted```. What could be wrong?

    * The firewall is rejecting IPv6 traffic.
    

* What is SNAT and when should it be used?

    * It is Source Network Address Translation and it should be used when a 
    node inside a private network needs to send data to a server outside the 
    private network.
    

* Explain how could you ssh login into a Linux system that DROPs all new 
incoming packets using a SSH tunnel.

    * By using a reverse ssh tunnel.


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
