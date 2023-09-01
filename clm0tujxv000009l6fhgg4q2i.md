---
title: "Linux File System Hierarchy"
datePublished: Fri Sep 01 2023 16:46:31 GMT+0000 (Coordinated Universal Time)
cuid: clm0tujxv000009l6fhgg4q2i
slug: linux-file-system-hierarchy
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693312883985/321a1235-aeb0-4a2a-9ed9-db6a979bc017.jpeg

---

In 🐧Linux everything is represented as a file📄 including a hardware program👨‍💻,

the files are stored in a directory📂.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693278901383/79dd972d-ddad-4596-9649-dde8b3c65654.png align="center")

* 🌱 **Root Directory (/)** 🏞️
    
    The base of the Linux directory is the root.Every directory arises from the root directory. It is represented by a forward slash (/).
    
* 🏠 **/root - Home of the Superuser** 🦸‍♂️
    
    It is the home directory for the root user (superuser).
    
* 💼 **/bin - User Binaries** 📊
    
    Contains binary executable and Linux commands
    
* 🏡 **/home - Home Sweet Home** 🏠
    
    it contain secondary users home directory.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693314789712/f6df92ee-3cd8-4deb-b90a-56faf7d0317d.png align="center")
    
* 📟 **/dev - Device Files** 📱
    
    Contains device files.
    
    These include terminal devices, usb, or any device attached to the system.
    
* 📦 **/var - Variable Files** 🧰
    
    Growing content finds its place here:
    
    * /var/log: Logs from OS and apps.
        
    * /var/lib: Databases and package files.
        
    * /var/mail: A home for emails.
        
    * /var/tmp: Temporary files for reboot resilience.
        
* 🏞️ **/mnt - Mounting Point** 🏔️
    
    When you need to temporarily mount a file system, this is the spot.
    
* 📀 **/media - Removable Media** 🖇️
    
    this directory contains removable media devices
    
* ⚙️ **/sbin - System Binaries** 🔧
    
    just lilke /bin ,/sbin also contains binary executables.
    
    in this directory linux commands are typical and used for system maintanance by system administrator.
    
* 🧑‍💼 **/usr - User Binaries** 👩‍💼
    
    this directory contains application and files used by users.
    
* **🔧/etc-&gt;configuration files of server⚙️**
    
* **🚀/boot-&gt;boot loader files🚀**
    
* **❄️/tmp-&gt;temporary files☃️**
    

If you connect with your Linux machine with the user name **ubuntu**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693311873674/9f0f0a13-a8e6-493d-808f-3e2fd5f8e82a.png align="center")

And then check your present working directory🚶 You realize you are in /home/ubuntu because ubuntu is not a superuser🦸‍♂️ That is why ubuntu(normal or secondary) world start from /home/ubuntu

```plaintext
ubuntu@ip-172-31-32-220:~$ pwd
/home/ubuntu
ubuntu@ip-172-31-32-220:~$
```

Now think where all other directories📁 like media , bin don't worry just run cd / to go to the root directory and list directories using ls

```plaintext
ubuntu@ip-172-31-32-220:~$ pwd
/home/ubuntu
ubuntu@ip-172-31-32-220:~$ cd /
ubuntu@ip-172-31-32-220:/$ ls
bin  boot  dev  etc  home  lib  lib32  lib64  libx32  lost+found  media  mnt  opt  proc  root  run  sbin  snap  srv  sys  tmp  usr  var
ubuntu@ip-172-31-32-220:/$
```

then type cd home then type cd ubuntu

now you reached where you started🗺️🏠

```plaintext
ubuntu@ip-172-31-32-220:~$ pwd
/home/ubuntu
ubuntu@ip-172-31-32-220:~$ cd /
ubuntu@ip-172-31-32-220:/$ ls
bin  boot  dev  etc  home  lib  lib32  lib64  libx32  lost+found  media  mnt  opt  proc  root  run  sbin  snap  srv  sys  tmp  usr  var
ubuntu@ip-172-31-32-220:/$ cd home
ubuntu@ip-172-31-32-220:/home$ cd ubuntu/
ubuntu@ip-172-31-32-220:~$ pwd
/home/ubuntu
ubuntu@ip-172-31-32-220:~$
```