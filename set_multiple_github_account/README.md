# Set Multiple GitHub Account
if you want to spearate the use of git for personal and work purposes, there is the need to manage multiple GitHub accounts on the same computer.  
## Generate the Multiple SSH Keys
Follow the step below the link
[setup_ssh_key](../setup_ssh_key/README.md)
For example, if generate two SSH keys, there should be
~~~
$ cd ~/.ssh
$ ls 
config  id_ed25519_work  id_ed25519_work.pub  id_ed25519_personal  id_ed25519_personal.pub
~~~
## Add the New SSH Key to the Corresponding GitHub Account 
Follow the step below the link
[setup_ssh_key](../setup_ssh_key/README.md)

## Modify the Config for the New GitHub Account 
~~~
# work account
Host github.com-work
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_work
# personal account
Host github-personal
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_personal
~~~

# Clone Project with Different Account
if want to clone a project by specified GitHub account, 
add `-personal` or `-work` after `github.com`
~~~
git clone git@github.com-personal:github_user/repo_name.git
~~~

# Set Different Account under Different Repositories
this approach can let you to operate different github accounts under different repositories.
~~~
# Clone and configure a personal repo
git clone git@github.com:github_user/personal-repo-dir.git
cd personal-repo-dir
git config --local user.name 'user1'
git config --local user.email 'user1@email.com'
~~~

~~~
# Clone and configure a work repo
git clone git@github.com:github_user/work-repo-dir.git
cd work-repo-dir
git config --local user.name 'user2'
git config --local user.email 'user2@email.com'
~~~


reference:

[[1]](https://chiahsien.github.io/post/how-to-use-different-ssh-key-for-different-github-account/)

[[2]](https://www.freecodecamp.org/news/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca/)

[[3]](https://tec.xenby.com/42-github-%E5%A4%9A%E5%B8%B3%E8%99%9F%E4%BD%BF%E7%94%A8%E4%B8%8D%E5%90%8C-ssh-key-%E8%A8%AD%E5%AE%9A%E6%8C%87%E5%8D%97)


[[4]](https://atornblad.se/use-a-different-user-account-for-each-git-repo)