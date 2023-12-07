### Instructions

Create a jenkins server on aws.

Create another ec2 on which the dockerized apps will be deployed. 

Connect this new node to jenkins.

Create a new item in Jenkins as pipeline. and use Jenkinsfile located at 
https://github.com/Awan/multi-tier-app.git root. 

Save and build it.


You will need something like if you want to push the artifacts to docker hub, 
you will need to add credentials in jenkins as dockerhub_credentials as 
Jenkinsfile has same ID as mentioned here.


