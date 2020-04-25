# Install Jenkins

First, we will install Jenkins by pulling Jenkins Docker image.

Execute `wget http://mirrors.jenkins.io/war-stable/latest/jenkins.war && java -jar jenkins.war`{{execute}}. This command will download `Jenkins.war` file and runs it.

By default, Jenkins listens on port 8080, which is exposed in you Dashboard on the right, or via https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/
