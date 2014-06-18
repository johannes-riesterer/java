Installing Oracle-Java on an Ubuntu system
  ===========
 
 
 Open a terminal and check what kind of operating system you are running.
 ```bash
 sudo  uname -m
 ```
 
 The output means:
- x86_64: 64 bit kernel
- i686: 32 bit kernel
 
 Corresponding to your operating system, download the  file ```jdk-newest-version.tar.gz``` from [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html?ssSourceSiteId=otnjp).
 
In what follows, please substitute ```jdk-newest-version``` with the appropriate filename!
 
Create the directory /opt/jdk:

```bash
sudo  mkdir /opt/jdk
```

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
