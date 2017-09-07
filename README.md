# Linux Server Configuration

Project for the Udacity Full Stack Web Developer Nanodegree Program.

## Submission

### 1. The IP address and SSH port so your server can be accessed by the reviewer.  
IP: `52.59.4.116` PORT: `2200`

### 2. The complete URL to your hosted web application.  
http://52.59.4.116

### 3. A summary of software you installed and configuration changes made.  
Installed packages: `apache2`, `postgresql`, `finger`, `libapache2-mod-wsgi`.
```
sudo apt-get update
sudo apt-get install apache2 postgresql finger libapache2-mod-wsgi
```

### 4. A list of any third-party resources you made use of to complete this project.  
1. [mod_wsgi (Apache)](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/)  
2. [How to create user for a db in postgresql?](https://stackoverflow.com/questions/10861260/how-to-create-user-for-a-db-in-postgresql)

### 5. Update all currently installed packages
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
```
### 6. Change the SSH port from 22 to 2200

1. Use `sudo vim /etc/ssh/sshd_config` and then change Port 22 to Port 2200 , save & quit.
2. Reload SSH using `sudo service ssh restart`

## 7. Configure the Uncomplicated Firewall (UFW)
```
ufw status
ufw allow 2200/tcp
ufw allow www
ufw allow ntp
ufw enable
ufw status
```
