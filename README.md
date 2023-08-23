Steps to follow:
- Launch an EC2 instance with Ubuntu AMI (Jenkins server).
- Install Jenkins on it.
- Download Maven Integration plugin on Jenkins server and go to Manage Jenkins -> Tools and update JDK and maven path
- Make a new Maven project and add your Github url and then run the job
- Jenkins pull the code from Github and create build artifacts which we have to deploy on Tomcat server
- Launch another EC2 instance with Ubuntu AMI (Tomcat server)
- Install Tomcat on it (https://www.digitalocean.com/community/tutorials/how-to-install-apache-tomcat-10-on-ubuntu-20-04)
- 
