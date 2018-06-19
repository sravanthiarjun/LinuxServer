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



