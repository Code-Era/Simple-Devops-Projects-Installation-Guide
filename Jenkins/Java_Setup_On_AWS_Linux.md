# Steps to set JAVA enviroment variable on Amazon Linux .


### Steps 
1. Check & install correct JAVA version
   - java --version
   - sudo yum list | grep openjdk -> for jdk 
   - sudo yum install java-1.8.0-openjdk.x86_64. -> For install jdk.
   
2. Find Actual location Java
  -$ file $(which java)
    /usr/bin/java: symbolic link to `/etc/alternatives/java'
  - copy `/etc/alternatives/java' path 
  - $ file /etc/alternatives/java
  - You will get path ->/usr/lib/jvm/jdk-1.8.0-openjdk.x86_64/bin
    
    
## Set JAVA environment variable 
1. Open .bash_profile file and set JAVA_HOME=/usr/lib/jvm/jdk-1.8.0-openjdk.x86_64/bin 
2. check with echo $JAVA_HOME


 
### Command 
   ```sh
  pwd -> Present work direcotry
  sudo su-
  cd ~  ->go to root
  clear -> clear screen
  ls -la -> print all bash profile file
  file $(which java) -> check java location
  /etc/alternatives/java -> copy this
  file /etc/alternatives/java -> give exact java location and copty that.
  sudo nano .batch_profile or vi .bash_profile -> to edit the file
  press Esc and :wq -> to save changes in file.
  echo $PATH
  echo $JAVA_HOME -> show nothing , you must have logout first.
  exit -> logout
  sudo su -  -> You have agin login as root 
  echo $JAVA_HOME

  
