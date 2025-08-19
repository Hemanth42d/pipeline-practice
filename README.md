# Build a Pipeline in jenkins.

In this repo I learned how to build a pipeline in jenkins in a google clouds VM instance and will be given a walkthrough how you guys can build the basic pipeline in jenkins.

[The java application used in this project can be found]([here](https://github.com/Hemanth42d/java-maven-app-learning-jenkins.git))

The thing we need to check before building a pipeline is:
- We need a server to run these services on (In my example i am using a Google clouds virtual machine )
- Install docker in it as i run the jenkins services as a docker container
- Then Follow the procedure in ui to build it as shown below.

Basically building a pipeline is not done in ui which is in the case of freestyle job (Most of freestyle job can be done using UI)

## Install docker in server and run the jenkins as a docker container.

[I have explained the way to do it in one of my repo and giving a link here go and check it out if you were not aware of running jenkins as a docker service.](click here)

After successfully installed docker and ran jenkins as a docker container we now need to login to jenkins and access the port 8080 or any port you have specified in while running the docker run command.

Once you access the jenkins server you will have the ui and click on the '+New Item' or ' Create new Job ' in the ui.

<img width="352" height="460" alt="jenkins_github" src="https://github.com/user-attachments/assets/58d17431-4ea4-4de8-b8c4-aa46a5ac60b6" />

click the + New Item or the one in the center of jenkins displays create a job if you are creating it for the first time.

1) Then choose **Pipeline** in the options and give it a name (ex: my-first-pipeline)
2) Then click on ok

Once clicking on ok you will be redirected to the pipeline configure page and need to configure some setting for the pipeline. They are

1) Under Pipeline in Defination click on the **Pipeline Script from SCM**
2) After clicking on scm now you need to select the SCM(source code management) in our case **Git**
3) Then we need to provide it the url of the repo and credentials configure their itself or you can redirect to credentials tab in manage jenkins and **here we are using UserNameWithPasswrod**
4) Then Choose the branch name you need to configure the pipeline for
5) At last we have an option i.e jenkinsfile path by default it will search in root folder with the name you specify their and leave it jenkinsfile (recommended)

<img width="1920" height="959" alt="Screenshot from 2025-08-19 23-18-37" src="https://github.com/user-attachments/assets/fad8b14f-55f7-4e81-84f1-c1b6e9c139c6" />

Then configure jenkinsfile like code code for the jenkins file , here i provide the link for jenkins file is in the application code itself.(mentioned above)
At last click on Build Now and check for error logs or success logs in the console output section.
After completion we will get success message and something like this

<img width="1920" height="959" alt="Screenshot from 2025-08-19 22-09-41" src="https://github.com/user-attachments/assets/fa00eeca-df26-4cf6-bc5e-963658c70cc8" />

so the pipeline has build and ran successfully!



