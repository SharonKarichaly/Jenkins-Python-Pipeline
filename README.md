
How to execute python script using the Jenkins pipeline
# What is Jenkins?

Jenkins is a continuous open-source integration written in Java. it is a Continuous Integration and Continuous delivery tool. We can orchestrate application deployments using Jenkins with a wide range of freely available community plugins and native Jenkins workflows.


<img width="580" alt="Screenshot 2022-07-26 at 9 25 53 PM" src="https://user-images.githubusercontent.com/106381638/181053140-4d2896d6-9cfa-4933-9f8e-c48916f3ba06.png">

Jenkins is commonly used for the following.
1. Continuous Integration for application and infrastructure code.
2. Continuously deliver pipeline to deploy the application to different environments using Jenkins Pipeline as a code
3. Infrastructure component deployment and management.
4. Run batch operations using Jenkins jobs.
5. Run ad-hoc operations like backups, cleanups, remote script execution, event triggers, etc

# Jenkins Pipeline
Jenkins pipeline allows us to define a complete list of events that happen in the code lifecycle. Starting from the build, to testing and deployment. 
We can use a set of plugins that help in the implementation of certain processes as a continuous delivery pipeline. Where pipelines are defined using code by using groovy language to define the processes that would run in the pipeline. 



# Objective
Here we are executing a python script job using the Jenkins pipeline

In this project I pushed my project code to GitHub which is linked with Jenkins, which is responsible to execute a python script job using the Jenkins pipeline



# About Python script

This is a simple python script used to fetch the below details from a server.

1.Hostname of the machine

2.IP address of the machine

3.Total available memory of the machine

4.Load average of the machine

5.Disk usage of the machine

I used socket and subprocess modules in the python to get this details.

# Creation of Jenkinsfile

Stage 1:
Use checkout option in pipeline syntax generator to link the repository with the Jenkins server and select the branch where code is present. since it's a public repository, I am not using any credentials/tokens.

Stage 2:
Use shell script option in pipeline syntax generator to execute the python script

Stage 3:
Use shell script option in pipeline syntax generator to redirect the terminal output to a file

Build and verify the stage logs


<img width="634" alt="Screenshot 2022-07-26 at 10 40 14 PM" src="https://user-images.githubusercontent.com/106381638/181068554-922ea044-6f7d-4024-bf1d-9b80f6d135c6.png">


Login to the server and verify the details in /var/lib/jenkins/workspace/Repository_folder/



<img width="929" alt="Screenshot 2022-07-26 at 10 46 08 PM" src="https://user-images.githubusercontent.com/106381638/181069760-4c5af464-a7f8-4bca-807d-c8704f628105.png">







