# Pre-requisites for this tutorial
Two Github accounts should be created before you begin this tutorial. More about how these two accounts will be used will come later in the tutorial.

# Introduction to DevOps
DevOps is a set of practices whose purpose is to have less segregation between the development and operation parts in software development life cycle. In general, these principles are about facilitating continuous integration and continuous delivery/deployment (CI/CD) using automation tools. A popular CI/CD tool is Jenkins, which is the topic of this tutorial.

# Introduction to Jenkins
Jenkins is CI/CD server that helps automate repetitive tasks in the software development and operation. Jenkins has many plug-ins that facilitate automating most tasks. Moreover, even if there is no plug-in that does what you want, you can always create your own. That is why Jenkins is very extensible and flexible.

For this tutorial, we are going to Jenkins `Multibranch Pipeline` plug-in, which helps create pipelines for software projects that are version controlled. A pipeline consists of different stages that you design to suit your needs. For example, in this tutorial, we create a pipeline that consists of stages that will take the project from version control to build, test, and deliver/deploy it in an automated manner. More details about this below under `Jenkins Multibranch Pipeline for this tutorial`.

# Sample Java App for this tutorial
For the purpose of this tutorial, a sample Java app hosted on a [Github repository](https://github.com/georgewbar/sample-project-repo) will be used to for tutorial. This app is a simple Java application that prints "Hello world" and has some unit tests for the purpose of this tutorial.

This repo will be forked in an organization that will be created in this tutorial. Moreover, in this tutorial, this repo will be configured to prevent directly pushing to the `master` branch, and to prevent merging code from other branches before reviewing the code and before Jenkins accepts the code by sending the commit status to Github.

# Jenkins Multibranch Pipeline for this tutorial
The pipeline that we are going to build in this tutorial will consist of the following ordered stages:

1. `Build` stage: The pipeline will first build the application to see if there are any syntax errors or dependency issues.
2. `Test` stage: If the build stage was successful, the pipeline will then run the unit tests.
3. `Deliver` stage: If the test stage had no failing unit tests, the pipeline will then package the application into a JAR file, and save it as an artifact.

As seen in the description above, if any the stage fail, all the following stages will not be executed and the pipeline will be marked as a failed pipeline.

Moreover, in this tutorial, we will configure Github webhooks to trigger the pipeline when new commits are pushed to any branch in the repo, and we will configure Jenkins to send a commit status as a response to Github to make Github accept merging the code after reviewing.

Render port 80: https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

Now, Let's begin the tutorial.
