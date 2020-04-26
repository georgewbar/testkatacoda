# Install Jenkins

First, we will install Jenkins by pulling Jenkins Docker image. Do the following steps in the terminal (or by clicking on each command directly; this will write the command in the terminal and will press ENTER):

1. Execute `wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -`{{execute}}. This command will add the repository key to Ubuntu. It will print  `OK` in the terminal.

2. Execute `echo deb https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list`{{execute}}. This command will add the package repo
address to the system.

3. Execute `sudo apt-get update && sudo apt-get install jenkins -y`{{execute}}. This will update the system to use the repo that was added in the previous steps to install Jenkins.

4. Execute `sudo systemctl start jenkins`{{execute}}. This command will start Jenkins. If this step does not work, please redo step 3 again and then continue to step 4 again, because Katacoda sometimes does not execute step 3 successfully from the first time.

5. If you want to get the status of Jenkins service, execute `sudo systemctl status jenkins`{{execute}}.

6. Then, execute `sudo usermod -a -G docker jenkins`{{execute}}. This will add the user `jenkins` to `docker` group. This is needed to give Jenkins the ability to start new containers, which we will need.

7. Then, restart Jenkins by executing `sudo systemctl restart jenkins`{{execute}} for that change to take effect. And, run `sudo systemctl status jenkins`{{execute}} to make sure that Jenkins is running.

By default, Jenkins listens on port 8080, which is exposed in your Dashboard on your right, or via   
https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/.  
I would advice using the link because it sometimes lags in the dashboard.

Normally, you would want to expose port 8080 in your firewall by executing `sudo ufw allow 8080`, or you could even use a proxy server that forwards requests Jenkins instead. However, for our purposes here, it is enough to execute up to step 5, because Katacoda already exposes port 8080 in your dashboard or via the link mentioned above.

# Change default password

Now, if you refresh the dashboard, you will see that Jenkins will show up (although it could take some time until it starts; you should wait until Jenkins starts before proceeding). Jenkins will tell you that you could find the default password in path `/var/lib/jenkins/secrets/initialAdminPassword`.

To get this password, execute `cat /var/lib/jenkins/secrets/initialAdminPassword`{{execute}}, which will print the default password on the terminal. Copy this password by marking it and right clicking, and clicking on Copy. Then, paste this password in the Jenkins.

This will open a new page where you need to create a new user. Fill in your desired data (I would advice using an easy username and password).

I will use `<USERNAME>` to indicate the username that was filled in the form. As an example, I will replace `<USERNAME>`=`devopsdev`. This means that the username that I will use to login is `devopsdev`.
