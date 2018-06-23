# LinuxServer

## This is the sixth project of Udacity Full Stack Nanodegree course.

#### Details About The Server:

Server IP address:13.127.121.235.xip.io 
UrlSite : http://13.127.121.235.xip.io

#### Grader Key:
      -----BEGIN RSA PRIVATE KEY-----
      MIIEpQIBAAKCAQEAx5RCM7/PsJ0osqLOV3Ra7YHoQT2jSSBgmfquCUJCbPxzS+rw
      SjtaashR++0Bai+V4dTtqzhgrfNGFGgfBcm5+LJuF4vJ/G+wzHLcRjpzlhloUsht
      lScQKfKJMm1hz3avyAaWCpxyJAfQjmjp1Ae2bee8NLi/abKnPsVS/1dAK44O0aj9
      01lZiO6IvzCNiXzuQHuoCjrf7/uX1ilNTHUUKNO9TWXkxexwyoKzFa9XJuQyADWe
      eJuyt+0duMHGoS5hsJibmogsHmXrX12h7F6WjhwCsBct8dcvUeZ3z3PH7Jj+KnvK
      xsGP77SxP1T4rOrtP7PFSYmeXm08s7P3SLCdcwIDAQABAoIBACPB/nKDJVUBc28+
      GDY3FKuFIPW/c2gAsw4jidcC1h/sw0OQ3miOZc7IAVhfyGccC4Cgw8xvl3LTKXUy  
      ioxg7j8OyQbS9ueRo12eHrU+d8Mm3jgmzOtySkUZvVcZnfKr0ybFd1CDYzftZoJ9
      bZedoiPi5yeTCkiHx8tJU2uIWGj1A76k2u/kL0M5F9srU1+CE/TbUDXeocJ4i5Cz
      LrureLkgQwonL/SLsxRI9qkWqVDAvOmy1zak7ndk0xMeYL7Z7eF0AhLEo0ufTaD5
      TFjWWwzBgx6lbR4oPA9s+U9eBVf8T4FD4oDFAJurHE8KhsB6ZRlCAU7IxpcPXVpS
      cmGv0GECgYEA7VwTtoeUZQBhGl3qlIOxpEHC+xkJpW+O2xh710EWXS4ISjAuM7mC
      2Em+r/uzul5TOj4nNGC5XsvT5XRFctCwOjYQSxgXnku+k+fQB0E6CjrqJMxGbOhg
      ATR+Nmc1yGQRfXVboYEIJpONo5YA3mS/fvJWHVfL1WHntqNqdmHFV5sCgYEA10Ci
      dMJC0LQmHAGJVE/COyYy9kIwwcgEIU7+ckafof43zWjHUkJFaZXTVxT7sNqpLObo
      PawBFpBqGGTlPfEjOT0vES3rV4evYZO+rHTAyMebCu32m4vmUoggr16TnwmEl6cO
      BuXkowic9aHaoEFt+uO7hgDIcCsXgFu6B890qwkCgYEArqNPkb3hbgrAZyDwhoL6
      wcrsxcjfMwyIhCVYgMDPzpEe4k7ev4nffnmLxnmf/CCIhdLTD5OW7+tyJWHN8zMe
      ZkX+6PF59yrttm8ZvSy9omdEfPybWGgEsv5HWonHpYAS6kbdu09visqHrPOiAf8I
      ckOlHoPJYl9dmCBWJXG8O78CgYEAm/3FPaRCU4kaTRV39lfOxJrMN9aECwruo0zh
      7OLtcLIQspWKTTylnPztKaCVPfdYvqegCoGKUFXb7U3BLACCrEqAv4xtjwNPwAEY
      H1aFF3xACc2l99eM1Ka+ORjrFkgJhPWVnr4f0V6+kOv4ykZgc39yOIx8tX0lDOps
      iJh5TjECgYEApy5kU28ldrxWv0H5hKT5wXeopxCVPSZrNyPf8MdzlC4DJPLL8a2Z
      3fUbX6lBCx5Pj8mYwy5ALy2jlUoL4szVhMkIagC95kWwxcEdBn3PdxLkfncAYsft
      vIJAU7fF2k2BW60KO4A0VA94ySUiXSaTignW42i49SriJ90B+46ySa4=
      -----END RSA PRIVATE KEY-----
      
#### Grader password:

      unix
#### Step:1

1. Create an amazon account https://aws.amazon.com/

2. Create an instance in lightsail.aws.amazon.com

3. Download putty.exe and puttygen.exe in putty.org

--Open Putty. give staticIP of instance as hostname.

select file downloaded from shh-keys eg: LightsailDefaultPrivateKey-ap-south-1.pem click ok.then save private, yes,
give some name.. save on desktop.then close it. now you will see a .ppk file on desktop.

From left tree, click on SSH. after, Auth. You will see browser button. click on browser, and select .ppk file
and click on open. press No. username ubuntu

4. Create static ip in lightsail and download it.

5. Open putty enter your ip and add private key address.

6. From left tree, click on SSH. after, Auth. You will see browser button.

7.Click on browser, and select .ppk file and click on open.

8. Press No.

now we are connected to ubuntu user.

##### To get Update all files:

      sudo apt-get update
      sudo apt-get upgrade
      
##### To create grader user:

      sudo adduser grader
      
##### To get another new user:

      sudo nano /etc/sudoers
      
##### To grant permissions:

      grader  ALL=(ALL:ALL) ALL
      
##### To create ssh keypair grader:

   Open new terminal and generate a key.
     
      ssh-keygen
      
   Now we are in ubunu user so change to grader user by using given command.
   
     su - grader
     
##### create a new folder .ssh and new authorized_file:

      mkdir .ssh
      
##### Copy the public keys with .pub extension and save the authorized file

      sudo nano .ssh/authorized_keys
      
##### Permissions to user:

      chmod 700 .ssh
      
      chmod 644 .ssh/authorized_keys
      
##### Then we can restart our server by using coomand:

      service ssh restart
      
##### Now we get log in to the grader with our private key generated:

      ssh -i .ssh/id_rsa grader@ipaddress 
      
##### Now changing the port number of ssh:

      sudo nano /etc/ssh/sshd_config
      
   Then change the port number from 22 to 2200
   
##### Now get login by using this command:

      ssh -i .ssh/id_rsa -p 2200 grader@ipaddress
      
##### To make changes for Root:

      sudo nano /etc/ssh/sshd_config
      
   Note:Make change PermitRootLogin no
   
##### To get security for firewall:

      sudo ufw allow 2200/tcp
      sudo ufw allow 80/tcp
      sudo ufw allow 123/udp
      sudo ufw enable
      
##### Check status:

      sudo ufw status
      sudo dpkg-reconfigure tzdata
      
#### Step-2

##### Software Requirements:

AWS account with lightsail service activated.

1)Python Pip

2)Postgres

3)httplib2

4)SQLAlchemy

5)Apache2

6)Flask

7)Virtualenv

8)Requests

9)Oauth2client

##### Installation Process for softwares:

           sudo apt-get install apache2		

           sudo apt-get install python-setuptools libapache2-mod-wsgi

           sudo a2enmod wsgi

           cd /var/www

           sudo mkdir FlaskApp

           sudo apt-get install git

           sudo apt-get install python-pip virtualenv

           sudo virtualenv venv

           sudo pip install Flask

           sudo pip install postgresql oauth2client httplib2 requests psycopg2

           cd /var/www/FlaskApp
 
           sudo rm -r FlaskApp
           
##### To get git clone we need to install git:

      sudo apt-get install git
      
##### Now get address of your itemcatalog project from github:

      sudo git clone https://github.com/name/item_catalog.git
      
##### To change the file name of our main project file:

      sudo mv project.py __init__.py
      
##### Now open that file and add json file:

      sudo nano __init__.py
   Add the following coding after importing files.
   
      PROJECT_ROOT = os.path.realpath(os.path.dirname(__file__))
      json_url = os.path.join(PROJECT_ROOT, 'client_secrets.json')
      
   Make sure change client_secrets.json to json_url.
   
   Then after save and exit:
   
      ctrl+o
      ctrl+x
      y
      enter
      sudo nano mv project.py FlaskApp.wsgi
      
  And write the below code in it.
  
      #!/usr/bin/python
      import sys
      import logging
      logging.basicConfig(stream=sys.stderr)
      sys.path.insert(0,"/var/www/FlaskApp/")
      from FlaskApp import app as application
      application.secret_key = 'Add your secret key'
      
#### create a virtual host file:

      sudo nano /etc/apache2/sites-available/FlaskApp.conf
   
   And paste the below code in it.
   
      <VirtualHost *:80>
 	ServerName mywebsite.com
 	ServerAdmin admin@mywebsite.com
 	WSGIScriptAlias / /var/www/FlaskApp/flaskapp.wsgi
 	<Directory /var/www/FlaskApp/FlaskApp/>
 		Order allow,deny
 		Allow from all
 	</Directory>
 	Alias /static /var/www/FlaskApp/FlaskApp/static
 	<Directory /var/www/FlaskApp/FlaskApp/static/>
 		Order allow,deny
 		Allow from all
 	</Directory>
 	ErrorLog ${APACHE_LOG_DIR}/error.log
 	LogLevel warn
 	CustomLog ${APACHE_LOG_DIR}/access.log combined
      </VirtualHost>
      
   Replace the below code in both database_setup.py and __init__.py
   
           engine = create_engine('postgresql://catalog:password@localhost/catalog')
   
##### Database creation:

   First we have to install postgresql.

###### Install postgresql:

      sudo apt-get install postgresql
      sudo su - postgres
      psql
      
###### create user:

      CREATE USER catalog WITH PASSWORD 'password';
      ALTER USER catalog CREATEDB;
      CREATE DATABASE catalog WITH user catalog;
Move postgres database to catalog:

      \c catalog
      REVOKE ALL ON SCHEMA public FROM public;
      GRANT ALL ON SCHEMA public TO catalog;
      \q
      exit
Now change the database connection in both database_setup.py and __init__.py as :

      engine = create_engine('postgresql://catalog:password@localhost/catalog')
      
Open google api console and changethe uri's

###### redirect URI

      http://ip.xip.io\login
      http://ip.xip.io\gconnect
      http://ip.xip.io\callback
      
 #### FINAL STEP:
 
      sudo service apache2 restart
      
For error checking :

      sudo nano /var/log/apache2/error.log
      
#### Finally we must restart our server:

      sudo service apache2 restart

Then go to webbrowser and type your ipaddress finaly we get our project.

#### Reference used:

https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
https://www.github.com

#### OUTPUT:

CLICK HERE http://13.127.121.235.xip.io/




     


