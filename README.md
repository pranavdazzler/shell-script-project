

jenkinslogtos3.sh
JENKINS LOG FILE > STORE IN S3 TO REDUCE COST (BEFORE STORED IN ELK , HIGH COST)
-------------------------------------------------------------------------------
how to automate the storage of Jenkins build logs using a simple script. We’ll read today’s build logs and upload them directly to an S3 bucket with AWS CLI. 

S3 is a cost-effective choice compared to ELK for storing logs long-term. If you’re into DevOps and looking to optimize your workflows, this is a must-watch. Let’s make log management simple and efficient!


AWS CLI NEEDED
INSTALL JENKINS FOR LOGS
CREATE A S3 BUCKET FOR STORING LOGS

WE ARE INSTALLING JENKINS ON EC2 AND INSTALL AWS CLI FOR CALLING S3

AWS CONFIGURE (on that ec2)
-----------------------------------
where the log file in jenkins
 cd /var/lib/jenkins/logs


job file
build log

if you enable versioning , it will be versioned
but it will not do like that because we are only doing once a day using crone tab, so versioning will not needed

To COnfigure cronjob

crontab -e
* * * * * /file.sh
       
      REFERENCE
https://youtu.be/bR6AbqZK4LQ?si=HD17hwC_mZicciPt
