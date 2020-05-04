After Git Install, Create an free AWS account.
In Aws Account 
        # Service -> Ec2 instance -> Launch Instance
        # Choose AMI(Amazon Machine Image) - Amazon Linux AMI 2018.03.0.
        # Configure Instance -> Disk Size.
        # Inside Add Tags 
                1. Add Another Tag -> Name as key && "Jenkins_Server".
        # In Secuirt Group.
                1. Add another Securiy Group name - "DevOps_Projects_SG" And one more rule with post 8080 (for jenkins).
                2. Then click on review and launch.
        # Now create KeyPair and downlaod that key-pair for login inside the server.
        # launch.
Use MobaXterm to run the Aws server .
                
