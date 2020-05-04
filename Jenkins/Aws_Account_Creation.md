# Create AWS Account and Login.
1. click one Service -> Ec2 instance -> Launch Instance -> Configure Instance -> Disk Size.
2. Then Add Another tag  Name as key && "Jenkins_Server" on Add Tag Page.
3. On Security Steps -> 
                1. Add another Securiy Group name - "DevOps_Projects_SG" And one more rule with post 8080 (for jenkins).
                2. Then click on review and launch.
      
Now create KeyPair and downlaod that key-pair file for login inside the server and launch/
       
       
       
#### Install MobaXterm to run the Aws server.
 1. Click on Session and Copy public id of aws server.
 2. Paste on SSh key and also upload Key-Value pair downloaded file.
 3. Then Run, now you are ruuning your virtual linux server.
