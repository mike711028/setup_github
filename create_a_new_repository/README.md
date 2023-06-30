# Create a New Repository
## Create a Folder in local device
create a working directory of your project and initialize the Git
~~~
$ mkdir new_project && cd new_project
$ git init
~~~

## Set the Specified Git Account
skip this if you only have one git account or use the default one. 
~~~
$ git config --local user.name "user2"
$ git config --local user.email "user2@email.com"
~~~

## Add a Remote Repository from GitHub
Go to GitHub and Create a New Repository 

<p align="center">
  <img src=../img/create_a_new_repo.png>
</p>

## Connect Local Folder and Remote Repository 
~~~
$ cd new_project 
// add something into the folder 
$ git add -A 
$ git commit -m "first commit"
$ git branch -M main  // change master name to main 
$ git remote add origin git@github.com:mike711028/new_project.git // connect to remote repo
~~~

reference:

[[1]](https://kbroman.org/github_tutorial/pages/init.html)

[[2]](https://www.freecodecamp.org/news/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca/)