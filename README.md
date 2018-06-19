# LinuxServer
About Server
## This is the sixth project of Udacity Full Stack Nanodegree course.
### This project is about Configuring the linux servers.
### Details About The Server:
Server IP address: 13.232.54.254
##### Url site : 
### To connect to grader:
#### Download the file that is having our private key when we created our instance in the lightsail amazon.com
#### Save the private key provided in your machine and run the command as follows:
      ssh -i path/to/privatekey -p 2200 grader@13.127.109.109
#### To get Update all files:
      sudo apt-get update
#### To create grader user:
      sudo adduser grader
#### To get another new user:
      sudo nano /etc/sudoers
#### To grant permissions:
      grader  ALL=(ALL:ALL) ALL
#### To create ssh keypair grader:
      ssh-keygen
#### This generate the public key and private key to the .ssh folder
#### To get change to the new user:
     su -grader
#### create a new folder .ssh and new authorized_file:
      mkdir .ssh
#### copy the public keys with .pub extension and save the authorized file
      sudo nano .ssh/authorized_keys
#### To get permissions for to user:
      chmod 700 .ssh
#### To prevent other user to write on file:
      chmod 644 .ssh/authorized_keys
#### Then we can restart our server by using coomand:
      service ssh restart
#### Now we get log in to the grader with our private key generated:
      ssh -i .ssh/id_rsa grader@ipaddress 
#### Now changing the port number of ssh:
      sudo nano /etc/ssh/sshd_config
      change the port number from 22 to 2200
#### Now get login by using this command:
      ssh -i .ssh/id_rsa -p 2200 grader@ipaddress



     


