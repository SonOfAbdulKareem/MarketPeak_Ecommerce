# Capstone Project- Introduction to Cloud Computing # 

### Tasks ###

**1. Implement Version Control with Git**

## 1.1. Initialize Git Repository ##

* Begin by creating a project directory named **"MarketPeak_Ecommerce"**

* Inside this directory, initialize a Git repository to manage your version control.

![mkdir](Images/1.Git-init.jpg)

## 1.2. Obtain and Prepare the E-Commerce Website Template ## 

* Instead of developing the website from scratch, you'll use a preexisting e-commerce website template. This approach allows you to focus on the deployment and operational aspects, rather than on web development. The actual web development is done by web/software developers on the project.

![download](Images/2.Download.jpg)

* Extract the downloaded template into your project directory.

![extract](Images/3.Extracted-to-directory.jpg)

## 1.3. Stage and Commit the Template to Git. ##

* Add your website files to the Git repository

* Commit your changes with a clear, descriptive message.

![add](Images/4.Git-add.jpg)

![commit](Images/5.Git-commit.jpg)

## 1.4. Push the code to your Github repository. ##

After initializing your Git repository and adding your e-commerce website template, the next step is to push your code to a remote repository on GitHub. This step is crucial for version control and collaboration.

* Create a Remote Repository on GitHub: Log into your GitHub account and create a new repository named
"MarketPeak_Ecommerce" Leave the repository empty without initializing it with a README, gitignore, or license.

* Link Your Local Repository to GitHub: In your terminal, within your project directory, add the remote repository URL to your local repository configuration.

![create](Images/6.Create-repo.jpg)
Click on the "New repository" 

![name](Images/7.Name-Create.jpg)
Name it as any title of your choice and click on "Create repository"

![link](Images/8.Linking-your-repoWithLocalTerminal.jpg)
Linking your new repository with your local trminal.

*Push your Code: Upload your local repository content to GitHub. Using this command `git push -u origin main`.

![error](Images/9.error-bcs-mainBranch-doesNot-exist.jpg)
Oops! I've got an error when I tried to run the push command, as it's written, the error occured because I'm currently on *master branch* and not in *main branch* in my Github. 

![shoot](Images/10.Troubleshoot-by-creatingMainBranch.jpg)
Troubleshoot: This would make us create the *"main branch"* before pushing to the main on GitHub.


![look](Images/11.HowYourRepoWill-look-like.jpg)
This is how your GitHub repository should look like.

**2. AWS Deployment.**
To deploy **"MarketPeak_Ecommerce"** platform, you'll start by setting up an Amazon EC2 instance:

## 2.1. Set Up an AWS EC2 Instance.

* Log in to the AWS Management Console.

![EC2](Images/12.EC2-Dashboard.jpg)
After you've logged in, click on the "services" above and then select EC2. 

* Launch an EC2 instance using an Amazon Linux AMI.

![name](Images/13.Input-name-and-select.jpg)
Name your instance and select "Amazon Linux" as instructed.

![launch](Images/14.Launch.jpg)
Then click on "Launch" below.

* Connect to the instance using SSH.

![ssh](Images/19.GivePermmision-paste.jpg)

## 2.2. Clone the repository on the Linux Server. ##

Before deploying your e-commerce platform, you need to clone the GitHub repository to your AWS EC2 instance. This process involves authenticating with GitHub and choosing between two primary methods of cloning a repository: SSH and HTTPS. To see the ssh or http link to clone your repository.

1. Navigate to your repository in github console.

2. Select the **code** as highlighted in the image below.

![navigate](Images/20.Navigate.jpg)

**Using SSH Method:**
* Generate SSH keypair using ssh-keygen.

![the-key](Images/21.Generate-key.jpg) 

* Display and copy your public key.
Using the command: `cat /home/ubuntu/.ssh/id_rsa.pub`

![ssh-key](Images/22.ssh-key.jpg)

* Add the SSH public key to your GitHub account.

![profile](Images/23.click-on-your-profile.jpg)

On your GitHub, click on your profile at the top right as shown above.

![set](Images/24.click-on-settings.jpg)
Then go ahead to click on settings.

![the](Images/25.sshANDG=key.jpg)

You'd need to click on SSH and GPG keys.

![new](Images/26.click-on-new.jpg)
Furthermore, by clicking on "New SSH key".

![title](Images/27.title-clickSSHKEY.jpg)
Give a title, then add SSH key.

![image](Images/28.en-email-for-this.jpg)
A result of adding your public key to your github.


* Use the SSH clone URL to clone the repository:

![use](Images/29.use-the-ssh-clone-URL.jpg)
Copy the repository from here.

Adn then clone with the command `git clone git@github.com:yourusername/MarketPeak_Ecommerce.git`

![alt text](Images/30.paste-and-type-yes.jpg)

The HTTPS Method is ignored because It's not needed.

## 2.3. Install a Web Server on EC2 ##

[Apache HTTP Server (httpd)](https://www.google.com) is a widely used web server that serves HTML files and content over the internet. Installing it on Linux EC2 server allows you to host **MarketPeak E-commerce** site:

* Install Apache web server on the EC2 instance. Note that httpd is the software name for Apache on systems using yum package manager.
`sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

This first updates the linux server and then installs httpd (Apache), starts the web server, and ensures it automatically starts on server boot.


![set](Images/31.install.jpg)

![install](<Images/32.install Apache.jpg>)
Insatlling Apache


## 2.4. Configure httpd for Website ##
To serve the website from the EC2 instance, configure ***httpd*** to point to the directory on the Linux server where the website code files are stored. Usually in ***/var/www/html.***

* Prepare the Web Directory: Clear the default httpd web directory and copy MarketPeak Ecommerce website files to it.

Using: 
`sudo rm -rf /var/www/html/*
sudo cp -r ~/MarketPeak_Ecommerce/* /var/www/html/`

![confi](Images/33.configure-http.jpg)

The directory ***/var/www/html/*** is a standard directory structure on Linux systems that host web content, particulatly for the ***Apache    http    Server.***

* Reload httpd: Apply the changes by reloading the httpd services.

![reload](<Images/40.reload apache.jpg>)
Note: ***httpd*** is also known as ***Apache***

## 2.5. Access Website from Browser ##

* With ***httpd***  configured and website files in place, ***MarketPeak_Ecommerce*** platform is now live on the internet:

* Open a web browser and access the public IP of ypur EC2 instance to view the deployed website.

![website](Images/34.Access-website.jpg)

### 3. Continous Integration and Deployment Workflow. ###

To ensure a smooth workflow for developing, testing, and deploying your e-commerce platform, follow this structured approach. It covers naking changes in a development environment, utilizing version control with Git, and deploying updates to your production server on AWS.

**Step 1:** Developing New Features and Fixes.

![branch](Images/35.branch-creation-switching.jpg)
Creation of a ***development branch*** and switching to it.

**Step 2:** Version Control with Git.

![add](Images/36.stage-changes.jpg)
Stage the changes for a commit.

![commit](Images/37.commit.jpg)
Commit your Changes.

![push](Images/38.push.jpg)
Push all changes to origin.

**Step 3:** Pull Requests and Merging to the Main branch.

![merge](Images/38.1.push-and-merge.jpg)
Checkout main and merge development.

**Step 4:** Deploying Updates to the Production Server.

![pull](Images/39.pull.jpg)
Pull the latest changes on the server.

![update](<Images/41.to-save-changes-and restart.jpg>)
To update the configuration with the new changes.

![reload](<Images/40.reload apache.jpg>)
Reload your Apache.

![Test](Images/42.New-updates.os-website.jpg)
Testing New Chaanges.


    











