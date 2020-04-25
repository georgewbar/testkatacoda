# Install Jenkins

First, we will install Jenkins by pulling Jenkins Docker image. Do the following step.

1. Execute `wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -`{{execute}}. This command will add the repository key to Ubuntu. It will print  `OK` in the terminal.

2. Execute `echo deb https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list`{{execute}}. This command will add the package repo
address to the system.

3. Execute `sudo apt-get update && sudo apt-get install jenkins`. This will update the system to use the repo that was added in the previous steps to install Jenkins.

By default, Jenkins listens on port 8080, which is exposed in you Dashboard on the right, or via https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/
