# Git Config Setting 

After set up SSH for GitHub, the first thing to do is setting up the name and email address 

~~~
$ git config --global  user.name "username"
$ git config --global  user.email "user@email.com"
~~~

and use the command below to show all variables set in config file, along with their values.

~~~
$ git config -l
user.email=user@email.com
user.name=username
~~~

use `--local` to specify the name and email address under specific repository

~~~
$ git config --local user.name "user2name"
$ git config --local user.email "user2@email.com"
~~~


reference:

[[1]](https://backlog.com/git-tutorial/tw/reference/config.html)

[[2]](https://ithelp.ithome.com.tw/m/articles/10266644)

[[3]](https://gitbook.tw/chapters/config/user-config)

