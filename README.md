Steps to follow:
- Launch an EC2 instance with Ubuntu AMI (Jenkins server).
- Install Jenkins on it.
- Download Maven Integration plugin on Jenkins server and go to Manage Jenkins -> Tools and update JDK and maven path
- Make a new Maven project and add your Github url and then run the job
- Jenkins pull the code from Github and create build artifacts which we have to deploy on Tomcat server
- Launch another EC2 instance with Ubuntu AMI (Tomcat server)
- Install Tomcat on it (https://www.digitalocean.com/community/tutorials/how-to-install-apache-tomcat-10-on-ubuntu-20-04)
- Now we Integrate Tomcat with Jenkins by installing Deploy to container plugin
- Add credentials of Tomcat deployer username to Jenkins global credentials
- Now create a new job to build code using maven and deploy artifacts to Tomcat server
  
   <img width="613" alt="image" src="https://github.com/satyam19arya/K8s_java_app_cicd/assets/77580311/9f4dde75-6531-42e1-8606-6a6663050dc0">



```
 <role rolename="manager-gui"/>
 <role rolename="manager-script"/>
 <role rolename="manager-jmx"/>
 <role rolename="manager-status"/>
 <user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status"/>
 <user username="deployer" password="deployer" roles="manager-script"/>
 <user username="tomcat" password="s3cret" roles="manager-gui"/>
```

Output:

  <img width="599" alt="image" src="https://github.com/satyam19arya/Deploy_artifacts_on_tomcat_server_jenkins_cicd/assets/77580311/2f071e7f-0e43-4fa0-8a87-66779a79df8f">
  

## Architecture:
<img width="565" alt="image" src="https://github.com/satyam19arya/Deploy_artifacts_on_tomcat_server_jenkins_cicd/assets/77580311/dc8c7d56-4b9d-40e8-a8be-ed84aa353c97">


