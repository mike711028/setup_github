# Setup SSH Key 
all operation under Linux system
## Generate an SSH Key for an Account 

the email address has to be the same with the email you register on github
~~~
$ ssh-keygen -t rsa -C "your-email-address"
~~~ 

When you are prompted to "Enter a file in which to save the key", press Enter to accept the default file location. 
(if the file name already exists, you can modify file name here to avoid overwriting)
~~~
$ ssh-keygen -t ed25519 -C "your.name@personal.com"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/mikeli/.ssh/id_ed25519): /path/.ssh/id_ed25519_test    
~~~

When you are prompted to type a passphrase, press Enter

~~~
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
~~~

SSH public key file will be stored in default paht(~/.ssh/xxx.pub)

