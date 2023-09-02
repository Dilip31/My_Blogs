---
title: "Basic Linux Commands and File Operations 🐧"
datePublished: Sat Sep 02 2023 18:05:45 GMT+0000 (Coordinated Universal Time)
cuid: clm2c4az1000209mbhwidb2ny
slug: basic-linux-commands-and-file-operations
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693314464941/d6756972-a0ff-43ff-a08a-7a7e1d10bcad.jpeg
tags: linux, developer, devops, 90daysofdevops, tws

---

Let's dive into some powerful Linux commands and file manipulation techniques:

🌐 **Kernel Information** 🖥️

* `uname`: Displays the kernel (OS) name.
    
* `uname -r`: Shows the kernel version.
    

📂 **Directory Navigation** 🚀

* `cd`: Changes the current directory.
    

🧹 **Screen Management** 📺

* `clear`: Clears the screen.
    

🤖 **User Insights** 👤

* `whoami`: Displays the currently logged-in user.
    
* `history`: Shows a list of previously used commands.
    
* `date`: Reveals the current date and time.
    

📝 **Creating Files and Directories** 📁

1. For a single directory: `mkdir /shubham`
    
2. For multiple directories: `mkdir dev qa test`
    
3. Creating nested directories: `mkdir -p /dev/qa/test/devops`
    
4. Creating numbered directories: `mkdir /student{1..10}`
    

📄 **Creating Files** 📝

* Creating single file: `touch notes`
    
* Creating multiple files: `touch python java react`
    
* Creating numbered files: `touch books{1..10}`
    

📦 **Copying and Pasting** 📋

**Syntax:**

```plaintext
cp <options> <source> <destination>
```

**Options:**

* `-r`: Stands for recursive. When copying directories, this option allows the `cp` command to copy not only the directory itself but also its contents and subdirectories.
    
* `-v`: Stands for verbose. This option makes the `cp` command display the details of each file as it is being copied, providing you with a more detailed output.
    
* `-f`: Stands for force. The `cp` command normally asks for confirmation before overwriting files. When you use the `-f` option, the command doesn't prompt you for confirmation and forcefully performs the copy.
    

```plaintext
cp -rvf source_folder destination_folder
```

* Copying files: `cp -rvf /root/anaconda-ks.cfg /home`
    
* Copying files starting with 'D': `cp -rvf /root/D* /home`
    

❌ **Removing Files and Directories** ❎

* Removing files/directories: `rm -rvf /india/pune`
    

🔀 **Moving and Renaming** 🔄

* Moving files/directories: `mv /home/shub /root/Desktop`
    
* Renaming files/directories: `mv dev devops`