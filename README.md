# How to fork, clone & push your changes using git command line on a Mac.
## GitHub login
Sign in to your [GitHub](https://github.com/login) Account.

If you’ve never used GitHub before, get a [GitHub](https://github.com) Account.

Copy and Paste the following public repository URL into your Browser: 

https://github.com/nobl9/writingtest

Click the Fork Icon to fork the public repository.

Fork creates a copy of the repository in your Github account for further changes.


## Cloning the fork using git command line
### Installing git command line tools on a Mac

Paste this command in your MacOS Terminal to install [homebrew](https://brew.sh):

```bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)```

Install git:

```$ brew install git```

Set your user name in Git:

```$ git config --global user.name “your_user_name”```

Confirm that you have set the user name correctly in Git:

```$ git config --global user.name```

Set your e-mail in Git: 

```$ git config --global user.email “your_e-mail@example.com“```

Confirm that you have set the e-mail correctly in Git:

```$ git config --global user.email```

## Cloning your fork repository

Go to your own Github repository and you will see a repository named writingtest.

Click Clone button in writingtest repository to get the HTTP URL.

Run the following command to clone your fork repository:

```$ git clone https://github.com/Natalee777/writingtest.git```

The command contains the URL obtained previously.


## Pushing the changes to your fork

Edit the README.md file in TextEdit or other Mac text editor.
Save your changes.

Run the following command to get into the writingtest directory on your Mac

```$ cd writingtest```

Run the following command to 

