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
 git push origin main or other branch ( push the changes to Github)
``` 
## Branches

Create a new branch 
```
git branch "dev" or "prod" or "test" 

```
- Delete Local branch

```
git branch -d branch-name
```

- Force Delete Branch , use capital "B"
```
git branch -D branch-name

```

- Delete remote branch

```
git push origin --delete branch-name
```



 ```
 git checkout -b "dev"
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

## Gitconfig User 

user.name is not necessarily your GitHub user.

- The value of user.name is the name you want to be associated with your commits in Git.
- This is the name that will appear as the author when you commit to a Git repository.

### Config for a specific Repo
```
git config user.name "Your Name"
git config user.email "Your Email "
```

- Check your Config
```
git config --list
```


### Config for all your repos 

```
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
- Check your Config

```
git config --global --list
```

Specific Repo


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