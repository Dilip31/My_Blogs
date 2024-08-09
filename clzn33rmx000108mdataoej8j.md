---
title: "linux part  2"
datePublished: Fri Aug 09 2024 19:12:44 GMT+0000 (Coordinated Universal Time)
cuid: clzn33rmx000108mdataoej8j
slug: linux-part-2

---

### Basic commands

| Commands | Description | Format |
| --- | --- | --- |
| pwd | Print Working Directory | pwd |
| ls |  |  |
|  | List Files and Directories | ls |
|  | to display files and directories in long format | ls -l |
|  | to display hidden files | ls -a |
| uname | shows the name of the kernel | uname |
|  | version of kernal | uname -r |
| clear | to clear screen | clear |
| whoami | shows currently login user name | whoami |
| history | shows list of previously used commands | history |
| date | shows time and date | date |
| cd | change directory |  |
|  | Change to Home Directory | cd |
|  | change to specific file | cd &lt;file name or specific loation&gt; |
|  | Move Up One Directory | cd .. |
|  | Change to the Previous Directory | cd - |

### create file and directories

|  |  |  |
| --- | --- | --- |
| mkdir | create sigle directory | mkdir &lt;name&gt; |
|  | create multiple directory | mkdir &lt;name&gt; &lt;name&gt; |
|  | for create directory inside directory | mkdir -p /dev/qa/test/devops |
|  | for create number of directory | mkdir student{1..10} |
| touch | for creating single file | touch &lt;name&gt; |
|  | for creating multiple files | touch &lt;name&gt; &lt;name&gt; |
|  | for cteating number of files | touch student{1..10} |

### copy , paste, remove, move and rename directories

|  |  |  |
| --- | --- | --- |
|  |  |  |
| cp | for copy and paste file and directory | cp &lt;option&gt; &lt;source&gt; &lt;destination&gt; |
|  |  | options -r recursive |
|  |  | \-v verbose |
|  |  | \-f forcefully |
|  | for copy file | cp -rvf &lt;source&gt; &lt;destination&gt; |
|  | for copy all data which start from D alphabet | cp -rvf /root/D\* /hom |
| rm | remove file or directory | rm -rvf &lt;location&gt; |
| mv | for move and rename file or directory | mv &lt;old location&gt; &lt;new location&gt; |

### user management

|  |  |  |
| --- | --- | --- |
| useradd | for create user account | useradd &lt;username&gt; |
| grep | for check user account properties | grep &lt;username&gt;/etc/passwd |
| passwd | for create user account password | passwd &lt;username&gt; |
| grep | for check user password properties | grep shub /etc/shadow |
| su | for switch user account | su &lt;username&gt; |
| exit | for log out from user account | exit or ctr+d key |
| userdel | for delete user account | userdel &lt;username&gt; |
| usermod | for change user login name | usermod -l &lt;old&gt; &lt;new&gt; |

### group management

|  |  |  |
| --- | --- | --- |
| groupadd | for add a group account | groupadd &lt;groupname&gt; |
| grep | To check group account property | grep &lt;groupname&gt; /etc/group |
| grep | To check group account property | grep &lt;groupname&gt; /etc/gshadow |
|  | to delete the group account | groupdel &lt;groupname&gt; |
| usermod | for adding a single member to the group | usermod -ag &lt;groupname&gt; &lt;username&gt; |
| gpasswd | for adding a single member to group | gpasswd -a &lt;username&gt; &lt;groupname&gt; |
|  | for adding multiple members to group | gpasswd -M &lt;username&gt; &lt;username&gt; &lt;groupname&gt; |
|  | to remove group member | gpasswd -d &lt;username&gt; &lt;groupname&gt; |
|  | To make group admin | gpasswd -A &lt;username&gt; &lt;groupname&gt; |
|  | print groups | sudo cat /etc/group |

### Linux file system permissions

```bash
ls -l /<filename>

-rw-r--. 1 root root 0 Jan 4 14:59 /notes.txt
```

* Permission
    
* Link
    
* Owner
    
* Group owner
    
* Size of file
    
* Date & time of file creation
    
* Name of file
    

```bash
    ls -ld /<directoryname>
```

|  | **Permission Representation** | **Ref** | **Octal representation** |
| --- | --- | --- | --- |
| **0** | No permission | \--- | 0 |
| **1** | Execute permission | \--x | 1 |
| **2** | Write permission | \-w- | 2 |
| **3** | Execute and write permission: 1 (execute) + 2 (write) | \-wx | 3 |
| **4** | Read permission | r-- | 4 |
| **5** | Read and execute permission: 4 (read) + 1 (execute) | r-x | 5 |
| **6** | Read and write permission: 4 (read) + 2 (write) | rw- | 6 |
| **7** | All permissions: 4 (read) + 2 (write) + 1 (execute) | rwx | 7 |

### changing permissions of file , user and group

|  |  |  |
| --- | --- | --- |
| chmod | Modifying permission via chmod | chmod nnn /&lt;filename&gt; |
| chown | to modify the owner of a file. | *chown &lt;owner name&gt; &lt;filename&gt;* |
| chgrp | to modify the group of the file. | *chgrp &lt;group name&gt; &lt;filename&gt;* |

### search word or files on linux

|  |  |  |
| --- | --- | --- |
| grep | to search single word from file | grep &lt;word&gt; filename |
|  | to search single word from anywhere | grep &lt;word&gt; /root/home |
| awk |  |  |
| find | to search .txt files | find \*.txt |
|  | to search files by group name | find &lt;fullpath&gt; -user &lt;username&gt; |
|  | to search files by user name | find &lt;fullpath&gt; -group &lt;groupname&gt; |

### ssh and scp

ssh-keygen -&gt;generate key pairs

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1694943170996/e62f569d-f803-4a9d-9ca5-f3c1499f5ea2.png align="center")

The `scp` command is used for securely copying files and directories between two different hosts in a network.

### manage system services

`systemctl` commands are used for managing system services and units on Linux systems

| Command | Description |
| --- | --- |
| `systemctl start [unit]` | Start a specific systemd unit (service or target). |
| `systemctl stop [unit]` | Stop a specific systemd unit (service or target). |
| `systemctl restart [unit]` | Restart a specific systemd unit. |
| `systemctl status [unit]` | Show the status of a specific systemd unit. |
| `systemctl enable [unit]` | Enable a systemd unit to start automatically at boot. |
| `systemctl disable [unit]` | Disable a systemd unit from starting automatically at boot. |