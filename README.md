2GitsOnOneComputer
==================

How to use 2 gits on one computer

* Set up one account that use more first normally.
* Generate 2nd SSH with different email ans save to different file
    ssh-keygen -t rsa -C "your-email-address"
    save to ~/.ssh/id_rsa_XXX.pub when asked
* Add ~/ssh/config as following:
```    
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa
Host github.com
    HostName github.com
    User chenyinl
  IdentityFile ~/.ssh/id_rsa_xxx
```

* Clone the new project with the link, please replace ":" with "/" and https://
```
git clone https://xxx@github.com/xxx/projectname.git
```

* Update the email 
```
git config --local user.email "xxx@domain.com"
```
* Try to push it should work now. Will ask for your password.
