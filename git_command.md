

# Install git in linux server
```
sudo yum -y install git  
```
# Configure the name and email address associated with git:
```
git config --global user.name "<YOUR NAME>"
git config --global user.email "<YOUR EMAIL>"
```
# Create an SSH key, using the default settings:
```
ssh-keygen -t rsa -b 4096
```
# Display the contents of our new public key (be sure to copy the key to your clipboard):
```
cat /home/cloud_user/.ssh/id_rsa.pub
```
# Log in to GitHub, navigate to Settings, click on SSH and GPG keys, and click on New SSH Key. Paste your public key information into this field and then click Add SSH key

### Create a Fork 
Create a personal fork of the sample repository https://github.com/linuxacademy/cicd-pipeline-train-schedule-git.

*Navigate to the URL https://github.com/linuxacademy/cicd-pipeline-train-schedule-git
*Click Fork in the top-right of the page.
Clone your personal fork from GitHub.

Click the green Clone or download button and copy the string that is displayed

In your terminal, run the following command:
```
cd ~/
git clone git@github.com:whboyd/cicd-pipeline-train-schedule-git.git
cd cicd-pipeline-train-schedule-git/
```
Create a feature branch to contain the change:
```
git checkout -b myBranch
```
Change the header text in 'views/index.jade' from “Train Schedule” to “Find your train!”:

vim views/index.jade
Add the change in 'views/index.jade' to the next commit:
```
git add .
```
Commit the change:
```
git commit -m "<UNIQUE MESSAGE>"
```
