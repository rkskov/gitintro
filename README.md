## Installing git
https://www.atlassian.com/git/tutorials/install-git

## Verify the installation
> git --version

## Set your user name
> git config --global user.name "Mona Lisa"
ß
## Creating a new local repository
In the root of the directory of your project type:

> git init

This creates a .git folder to hold the repository
Try listing the contents

> ls .git

## Cloning an existing remote repository
Navigate to the directory where you want your new project folder to appear and type:

> git clone rkskov@github.com:gitintro

## Adding files to the repository
Create a new file called example.txt
Then add it to the repository with

> touch example.txt
> git add example.txt

Now the repository is aware it's a file we want to track (it's in the index), but it has not yet been comitted

## Commiting changes
Lets go ahead and commit the first version of our example.txt file

> git commit -m "First commit"

Make sure to give et a good description for the benefit of others
Now the file has been comitted to your local repository, but nobody else can see it

## pushing changes to a remote repository

Lets push our change to the remote repository

> git push origin master

Because we cloned from a remote repository git already knows where to push the updates to. "origin" is the shorthand name for the remote repository you cloned from and "master" is the name of the branch to push to.

Often this is not the case and you have to set the remote server

> git remote add origin https://github.com/rkskov/gitintro.git

Maybe you have cloned somebody elses repository but want to push changes to your own remote repository.

## Ignoring build files 
Often you do not want build files to be part of the repository.
To ignore certain files create a .gitignore file

> touch .gitignore
> touch untracked.txt

Add a pattern to the .gitignore file to ignore untracked.txt.
Then add all files in the folder 


## Listing the files that are tracked by our index 
Lets list the files tracked now

> git ls-tree -r HEAD --name-only
