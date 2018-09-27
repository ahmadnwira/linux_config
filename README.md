# linux_config

public ip adress: 18.130.6.41
ssh port: 2200
user: grader

## Configuration

* Created user `grader` with command: useradd 
   $ adduser grader

* Add `sudo` privilage to grader copied manually the default user file from /etc/sudoer.d

* Allow `grader` to have ssh access
	* created key-pari using ssh-keygen on my local machine
	* installing the public key on the host server
	* mkdir /home/grader/.ssh / tocuh .ssh/authorized_keys
	* copy the content of public key in authorized_keys
	* chmod 700 /home/grader/.ssh
	* chmod 644 /home/grader/.ssh/authorized_keys

* Disable root login PermitRootLogin no
* change ssh port to 2200 from 22 
	* edit file /etc/ssh/sshd_config to set Port 2200
## UFW Setup
* sudo ufw allow 2200/tcp
* sudo ufw allow www
* sudo ufw allow ntp
* sudo ufw deny 22
* sudo ufw enable


   
## installed software 
 * pip3, postgres, flask
## resources
* https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps

* http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/
