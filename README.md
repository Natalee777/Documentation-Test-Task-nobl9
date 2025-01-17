# How to fork, clone push & merge your changes using git command line on a Mac
## GitHub login
* Sign in to your [GitHub](https://github.com/login) Account. If you’ve never used GitHub before, get a [GitHub](https://github.com) Account
* Copy and Paste the following public repository URL into your Browser: 
https://github.com/nobl9/writingtest

* Click the Fork Icon to Fork the public repository

![Screenshot Fork_Icon](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/ForkIcon.png)

Fork creates a copy of the repository in your Github Account for further changes.

## Cloning the fork using Git command line
### Installing git command line tools on a Mac

* Paste this command in your MacOS Terminal to install [homebrew](https://brew.sh)

```bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)```
* Install **Git**

```brew install git```
* Set your user name in **Git**

```git config --global user.name “your_user_name”```
* Confirm that you have set the user name correctly in **Git**

```git config --global user.name```
* Set your e-mail in **Git**

```git config --global user.email “your_e-mail@example.com“```
* Confirm that you have set the e-mail correctly in **Git**

```git config --global user.email```

### Adding a new SSH key to your GitHub account (optional)

* Run the following command in your MacOs Terminal to generate a new SSH key

```ssh-keygen -t rsa -b 4096 -C "your_email@example.com"```

* To accept the default file location, press Enter after the promt "Enter a file in which to save the key,"

![Screenshot SSH_key](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/SSH%20key%20Output.png)

* Run the following command in your MacOs Terminal to start the ssh-agent in the background

```eval "$(ssh-agent -s)"```

![Screenshot SSH_key_2](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/SSH%20Key%202.png)

* Run the following command to add your SSH private key to the ssh-agent 

```ssh-add -K ~/.ssh/id_rsa```

![Screenshot SSH_key_3](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/SSH%20Key%203.png)

* Run the following command to Copy the SSH key to your clipboard

```pbcopy < ~/.ssh/id_rsa.pub```

* Open GitHub, click your profile photo, then click **Settings**

![Screenshot GitHub_Settings](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/GitHub%20Settings.png)

* In the user settings sidebar, click **SSH and GPG key**

![Screenshot GitHub_Settings_2](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/GitHub%20Settings%202.png)

* Click **New SSH key**

![Screenshot GitHub_Settings_NewSSHKey](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/GitHub%20Settings%20NewSSHKey.png)

* Add a descriptive label in the "Title" field. 

* Paste your key into the "Key" field

![Screenshot GitHub_Settings_SSHForm](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/GitHubSettings%20SSH%20Form.png)

* Click **Add SSH key**

* If prompted, confirm your GitHub password


### Cloning your fork repository

* Go to your own Github repository and find the repository named **writingtest**

**Option 1: cloning your fork repository  using HTTPS**

* Click **Code** button in **writingtest** repository to get the HTTP URL

![Screenshot Get_Code](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/GetCode.png)

*  Run the following command in your MacOS Terminal to clone your fork repository

```git clone https://github.com/Natalee777/writingtest.git```

The command contains the HTTPS URL obtained previously.

**Option 2: cloning your fork repository using SSHkey, prerequisite: SSH key added to your Github Account, optional**

* Click **Code** button in **writingtest** repository to get the SSH key

![Screenshot Get_Code_SSH](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/GetCodeSSH.png)

*  Run the following command in your MacOS Terminal to clone your fork repository

```git clone git@github.com:Natalee777/writingtest.git```

The command contains the host alias obtained previously.

## Pushing the changes to your fork

* Edit the *README.md* file in TextEdit or other Mac text editor. Save your changes
* Run the following command to get into the **writingtest** directory on your Mac

```cd writingtest```

* Run the following command to see a hidden git folder in your **writingtest** directory

```git init```

* Run the following command to see the current status of your local repository

```git status```

You should see *README.md* marked as modified.

![Screenshot Output_Terminal](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Terminal.png)

* Run the following command to add this change

```git add README.md```

The command contains the name of the modified file.

* Run ```git status``` command again to see the changes ready to be commited

![Screenshot Output_Terminal_2](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Teminal%202.png)

* Run the following command to commit the changes

```git commit -m "Add a comment about the change"```

![Screenshot Output_Terminal_3](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Teminal%203.png)

* Run ```git status``` command again to check that everything is up to date

![Screenshot Output_Terminal_4](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Terminal%204.png)

* Run the following command to see what remote repository on Github our local repository is connected to

```git remote -v```

![Screenshot Output_Terminal_5](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Terminal%205.png)

* Run the following command to push the changes to the repository

```git push origin master```

![Screenshot Output_Terminal_6](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Terminal%206.png)

* Make sure your remote repository has been updated on Github
![Screenshot Update_GitHub](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/UpdateGitHub.png)

## Merging your commit into the public repository

* Click **New pull request** button to create your Pull Request

![Screenshot New_Pull_Request](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/New%20Pull%20Request.png)

* Click **compare across forks** to compare your repository with public repository

![Screenshot Compare_Across_Forks](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Compare%20Across%20Forks.png)

* Make sure the base repository is the public repository where changes should be applied while head repository contains the changes  

![Screenshot Base_Compare_Master](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/BaseCompareMaster.png)

* Type a Title and Description for your Pull Request

![Screenshot Title_Details](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/TitleDetails.png)

* Press **Create pull request** button
