2GitsOnOneComputer
==================

How to use 2 gits on one computer

1. Set up one account that use more first normally.
2. Generate 2nd SSH with different email ans save to different file
    ssh-keygen -t rsa -C "your-email-address"
    save to ~/.ssh/id_rsa_XXX.pub when asked
3. Add ~/ssh/config as following:
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

4. Clone the new project with:
```
git clone xxx@github.com/xxx/projectname.git
```

5. Update the email 
```
git config --local user.email "xxx@domain.com"
```
6. Try to push it should work now. Will ask for your password.
