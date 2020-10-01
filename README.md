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

```$ brew install git```
* Set your user name in **Git**

```$ git config --global user.name “your_user_name”```
* Confirm that you have set the user name correctly in **Git**

```$ git config --global user.name```
* Set your e-mail in **Git**

```$ git config --global user.email “your_e-mail@example.com“```
* Confirm that you have set the e-mail correctly in **Git**

```$ git config --global user.email```

### Adding a new SSH key to your GitHub account (optional)
* Run the following command in your MacOs Terminal to generate a new SSH key

```ssh-keygen -t rsa -b 4096 -C "your_email@example.com"```

* To accept the default file location, press Enter after the promt "Enter a file in which to save the key,"

![Screenshot SSH_key](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/SSH%20key%20Output.png)

* Run the following command in your MacOs Terminal to start the ssh-agent in the background

```eval "$(ssh-agent -s)"```


### Cloning your fork repository

* Go to your own Github repository and find the repository named **writingtest**

* Click **Code** button in **writingtest** repository to get the HTTP URL

![Screenshot Get_Code](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/GetCode.png)

*  Run the following command in your MacOS Terminal to clone your fork repository

```$ git clone https://github.com/Natalee777/writingtest.git```

The command contains the URL obtained previously.


## Pushing the changes to your fork

* Edit the *README.md* file in TextEdit or other Mac text editor. Save your changes
* Run the following command to get into the **writingtest** directory on your Mac

```$ cd writingtest```

* Run the following command to see a hidden git folder in your **writingtest** directory

```$ git init```

* Run the following command to see the current status of your local repository

```$ git status```

You should see *README.md* marked as modified.

![Screenshot Output_Terminal](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Terminal.png)

* Run the following command to add this change

```$ git add README.md```

The command contains the name of the modified file.

* Run ```$ git status``` command again to see the changes ready to be commited

![Screenshot Output_Terminal_2](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Teminal%202.png)

* Run the following command to commit the changes

```$ git commit -m "Add a comment about the change"```

![Screenshot Output_Terminal_3](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Teminal%203.png)

* Run ```$ git status``` command again to check that everything is up to date

![Screenshot Output_Terminal_4](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Terminal%204.png)

* Run the following command to see what remote repository on Github our local repository is connected to

```$ git remote -v```

![Screenshot Output_Terminal_5](https://github.com/Natalee777/Documentation-Test-Task-nobl9/blob/main/Output%20Terminal%205.png)

* Run the following command to push the changes to the repository

```$ git push origin master```

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
