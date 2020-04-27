# Invite a collaborator with `Write` access

Now we are going to add a new Github collaborator to your organization's Github repo fork. Call this new Github collaborator `<GITHUB_WRITE_USER>`. In my case here, `<GITHUB_WRITE_USER>`=`georgewba2015`.

(As a reminder, the admin Github in my case is `<GITHUB_ADMIN_USER>`=`georgewbar`)

Also, from now on, we will call the current browser that you have open right now `Browser_Admin`. Moreover, for the rest of this tutorial, I am also assuming that in your `Browser_Admin`, you have at least three tabs open: one tab for your `<GITHUB_ADMIN_USER>` account on Github, one tab for Katacoda tutorial, and one tab for the Jenkins server via URL https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/.

Now, do the following steps:

1. Now, in `BrowserAdmin`, go to your organization's repo fork `https://github.com/<ORGANIZATION ACCOUNT NAME>/sample-project-repo`{{copy}} (and sign in as `<GITHUB_ADMIN_USER>` if you are not already), where `<ORGANIZATION ACCOUNT NAME>` is replaced by your organization's account name. In my case, this URL is `https://github.com/devops-pipeline-tutorial/sample-project-repo`. Then, click on your repo settings.
![](./assets/settings_org.png)

1. Then, click on `Manage access` on the left.  
![](./assets/manage_access.png)

1. Then, click on `Invite teams or people`.  
![](./assets/invite.png)

1. Now, a new form will appear. Fill in the collaborator Github account name `<GITHUB_WRITE_USER>`. In my case, `<GITHUB_WRITE_USER>`=`georgewba2015`. Then, under `Choose a role`, select `Write`. Then, click on `Add <GITHUB_WRITE_USER> to sample-project-repo`.  
![](./assets/invite_form.png)

1. By now, an invitation email should have been sent to the email associated with the `<GITHUB_WRITE_USER>` account.

1. Now, open a totally different browser or an incognito browser (call it `Browser_Write`). For example, if `Browser_Admin` is a Chrome browser, open an `Incognito New Window` as your `Browser_Write`. Then, in `Browser_Write`, first sign in to your `<GITHUB_WRITE_USER>` Github account.  
> Note that: You could also do the same steps in the rest of this tutorial with only one browser. However, you would need to sign out your `<GITHUB_ADMIN_USER>` account and sign in to `<GITHUB_WRITE_USER>` account every time you need to access to `<GITHUB_WRITE_USER>` account, and you would do vice versa when you need access to `<GITHUB_ADMIN_USER>` instead. This is made easier by having two browsers instead as mentioned in this tutorial.

1. Then, in `Browser_Write`, open a new tab and sign in to the email associated with `<GITHUB_WRITE_USER>`. You should have gotten an invitation email similar to the email you see below (except that `devops-pipeline-tutorial/sample-project-repo` is replaced with `<ORGANIZATION ACCOUNT NAME>/sample-project-repo`). Click on `View invitation`.
![](./assets/invitation_on_email.png)

1. This will open a new page. Click on `Accept invitation`. Note that, in the image, `georgewbar` is replaced by `<GITHUB_ADMIN_USER>`.
![](./assets/accept_invite.png)

Now, `<GITHUB_WRITE_USER>` user should have `Write` access to the repo fork  `<ORGANIZATION ACCOUNT NAME>/sample-project-repo`.
