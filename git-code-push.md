# Create new token
## generate new token from 
### setting > Developer Settings > Generate new token (this token will be consider as your password) > save on safe place 

# Create new repository 
initialize git on your terminal 
```
git init
```

set Branch as Main
```
git branch -M main
```
check status of files
```
git status
```
add all the files to git for commit
```
git add README.md defaults/ handlers/ meta/ tasks/ tests/ vars/
```
Need to generate new remote directory to git, first check with 
```
git remote -v
```
set destination past for remote directory
```
git remote add origin https://github.com/zeeshankanuga/ansible-jenkins-install.git
```
apply
```
git commit -m "add all ansible jenkins file to git repository"
```

## finally push files to remote repository

```
git push origin main
```
``Username for 'https://github.com': zeeshankanuga`` write your user name
``Password for 'https://zeeshankanuga@github.com':`` passwork as yuo have generated token initially 
