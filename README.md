![Alt text](https://raw.githubusercontent.com/johannes-riesterer/java/master/imaginary_manuals.png)
==============
Installing Oracle-Java
===========

Linux
---------------
 
 
 Open a terminal and check what kind of operating system you are running. Type in
 ```bash
 uname -m
 ```
 
 The output:
- `x86_64` stands for _64 bit kernel_
- `i686` stands for _32 bit kernel_
 

Corresponding to the type of your operating system, download the  file ```jdk-newest-version.tar.gz``` from [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html?ssSourceSiteId=otnjp).
Linux x64 is for a 64 bit kernel and x86 for a 32 bit kernel.
![Alt text](https://raw.githubusercontent.com/johannes-riesterer/java/master/bd.png)

In what follows, please substitute ```jdk-newest-version``` with the appropriate filename!
 
Create the directory /opt/jdk. Therefore Type in the command
```bash
sudo mkdir /opt/jdk
```
and enter your password as asked for.

Extract the downloaded file jdk-newest-version.tar.gz to the created folder /opt/jdk:

```bash
sudo tar -zxf jdk-newest-version.tar.gz -C /opt/jdk
```

You will find the extracted files in /opt/jdk/jdk-newest-version.

Set oracle-jdk as the default java-virtual-machine:
```bash
sudo update-alternatives --install /usr/bin/java java /opt/jdk/jdk-newest-version/bin/java 100
sudo update-alternatives --install /usr/bin/javac javac /opt/jdk/jdk-newest-version/bin/javac 100
```

Check your installation:

```bash
java -version
```

The output should look like 
```bash
Java version "1.8"
    Java(TM) SE Runtime Environment (build 1.8)
    Java HotSpot(TM) 64-Bit Server VM (build 25.5-b02, mixed mode) 
```
