# Linux Server Configuration - Udacity
The goal of this project was to launch linux servers and configure them to then deploy a functional web app.

# IP address and ports
IP: 34.205.17.125
SSH Port: 2200
URL to site: http://34.205.17.125.xip.io/

# SUMMARY OF PROJECT

## Launch server
* I used amazon ec2 instance, differs a bit from amazon lightsail instances.
* updated and upgraded packages
* changed the ssh ports from default to another
* configured the firewall using uncomplicated firewall (UFW), allows some ports that I need and denied the rest.
* configured the ports from es2 instance dashboard
* made a new user to the server and gave it sudo access
* created a key pair using ssh-keygen tool
* configured the timezone for the server

## Pre deployment
* Installed Apache2
* Installed mod_wsgi for python3 and enabled it
* Intalled Postgresql and removed remote connections
* created a user for the database
* created the database needed
* installed git

## Deployment
* cloned my catalog project to the server
* changed ownership of all project files
* renamed python application file to __init__.py
* modified a number of files that contain database engines to work with the Postgresql
* updated OAuth client_secrets files for the new URLs and modified the path and client ID in some files.
* installed a virtual environment and libraries such as:
`pip install httplib2
pip install requests
pip install --upgrade oauth2client
pip install sqlalchemy
pip install flask
sudo apt-get install libpq-dev
pip install psycopg2`
* created a virtual host and enabled it to work with flask
* populated the data
* disabled the default apache site and enabled the new one
* changed all project files ownership to www-data:www-data
* fixed and updated a couple of errors after launching the webapp



## 3rd party resources and other 
* Installed fail2ban to prevent server attacks
* Installed unattended-upgrades to do automatic improtant updates
