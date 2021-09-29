# maven_build_deploy-HW3
By Samah Abbas - Fursa DevOps course


#### HW instuctions:
- Install Tomcat 9 on a server (new Instance) with Java 11
- Create a new Build Job to build the https://github.com/jleetutorial/maven-project.git
- Store the Archive file on Jenkins
- Create a second job called “deploy” to deploy the war file artifact on Tomcat
- Please convert the Jobs into new Jenkins Pipelines using Jenkins DSL)

#### Solution steps:
- created new server in EC2 
- install JDK 11 on the new server
- install tomcat9 on the new server
- created this repo in git
- created a jenkins pipeline job
- added the git repo to the jenkins job
- created the JenkinsFile
- created the pipline with 4 stages : clone stage ,build stage, archive the artifact, deploy.
- push it to the git repo
- and run the jenkins job on any availble server (with Maven installed on it)

