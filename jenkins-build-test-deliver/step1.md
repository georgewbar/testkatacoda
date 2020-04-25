# Install Jenkins

First, we will install Jenkins by pulling Jenkins Docker image. Do the following steps in the terminal (or by clicking on each command directly; this will write the command in the terminal and will press ENTER):

1. Execute `wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -`{{execute}}. This command will add the repository key to Ubuntu. It will print  `OK` in the terminal.

2. Execute `echo deb https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list`{{execute}}. This command will add the package repo
address to the system.

3. Execute `sudo apt-get update && sudo apt-get install jenkins -y`{{execute}}. This will update the system to use the repo that was added in the previous steps to install Jenkins.

4. Execute `sudo systemctl status jenkins`{{execute}}. This command will start Jenkins.

5. If you want to get the status of Jenkins service, execute `sudo systemctl status jenkins`{{execute}}.

By default, Jenkins listens on port 8080, which is exposed in your Dashboard on your right, or via https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/.

Normally, you would want to expose port 8080 in your firewall by executing `sudo ufw allow 8080`, or you could even use a proxy server that forwards requests Jenkins instead. However, for our purposes here, it is enough to execute up to step 5, because Katacoda already exposes port 8080 in your dashboard or via the link mentioned above..
