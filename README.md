# Project: Linux Server Configuration
This project uses sqlite database by Python3 that implements website reads categories and items information from a database. also,
to insert,update and delete items (CRUD) that belongs to you after signing in with google +. This project has been migrated into Ubuntu server with host: http://flaskef.ddns.net/
IP Address: http://18.191.201.100/
The server ip address linked to a free host that have been registerd and configured by https://www.noip.com/

# Getting Started
To start on this project, visit the website: http://flaskef.ddns.net/

# Installing
you need to have gmail account to login with google + 

# Running the tests and Deployment
To run this project using your Git Bash terminal for checking the server configurations, you need to type this command to login using ssh with port 26 as requested:

$ ssh grader@ec2-18-191-201-100.us-east-2.compute.amazonaws.com -p 26 -i ~/.ssh/id_rsa

then, Enter passphrase for key as: udacitygrader 
if you would like to switch to root user, just type  sudo su -
then password as: grader

you could visit the website: 
http://flaskef.ddns.net/

that points to ip: 
http://18.191.201.100/

when login into website and the google + hang in a white page just refresh the page.

A summary of configuration changes made 
1. Update all currently installed packages.
2. Change the SSH port from 22 to 2200. Make sure to configure the Lightsail firewall to allow it.
3. Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
4. Create a new user account named grader.
5. Give grader the permission to sudo.
6. Create an SSH key pair for grader using the ssh-keygen tool.
7. Configure the local timezone to UTC.
8. Install and configure Apache to serve a Python mod_wsgi application.
my project with Python 3, so i need to install the Python 3 mod_wsgi package on my server: 
sudo apt-get install libapache2-mod-wsgi-py3.
9. Install and configure PostgreSQL as requested, even if i did noy need it.
10. i need to install flask,sqlalchemy .. etc. for testing to run my source file app.py in my server after migration.
use this line to list the installed software packages on the server
sudo apt list --installed

for testing server side:
sudo nano -f /var/log/apache2/error.log 

for testing browsing side:
in google chrome press Ctrl + Shift + j

# Built With
Git Bash 
virtual machine
vagrant
Sublime Text editor
AWS EC2 Ubuntu

# Authors
HADIL SALEH ALSUDIES

# Acknowledgments
All the activities we have done during the virtual session by: MS. MASHAEL ELSAEEDI helped me, Thank you MS. MASHAEL.