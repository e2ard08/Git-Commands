# Practice GIT Commands for Certification 

## Basic Commands 
 
 to check the actual state of the branch
 ```
 git status
``` 

to make changes , use add , commit and Push 

 ```
 git add /e2.txt  ( an specific file ) 

 git add .  ( add all the files using ".")
``` 
 ```
 git commit -m "firts-comit"
``` 
 ```
 git push  ( send the changes to Github)
``` 
## Branches

 ```
 git checkout
 ``` 


##


- git commit -amend --no-edit
- git checkout --
- git reset HEAD 

- git reset --hard HEAD^
- git revert --no-edit
- git log 
- git push 

## Gitconfig File

```
git config --list 
```

## SSH Conection 

Create your Key 

```
ssh-keygen -t ed25519 -C "email@email.com" -f ~/.ssh/id_XXXX
```

Configure the Config file or Create a new one 

```
Path --->  ~/.ssh/config  vim config 
```

```
# GitHub
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_XXXX

    ( ----> save with :wq! <----)
```
Copy the Public Key and added into Github Settings > SSH Key 

```
cat ~/.ssh/id_XXXX.pub

ssh-ed25519 AxxXXxTTTPPOOO1258KKLDLDKJSDHHDHF YourEmail@XXX.com

```
Test the Connection 

```
ssh -T git@github.com
Hi ed! You've successfully authenticated
```