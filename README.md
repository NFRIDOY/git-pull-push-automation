# git-pull-push-automation

# Table of Contents

1. ✨ [Dangerous Pull and Push Bat Files](#dangerous-pull-and-push-bat-files)  
   1.1. 💥 [Use it Very Carefully](#use-it-very-carefully) 
2. ✨ [Prerequisite](#prerequisite)  
3. ✨ [Dangerous Pull and Push Specific Branch bat file](#Dangerous-Pull-and-Push-Specific-Branch-bat-file)

## ✨ Dangerous pull and push bat files
### 💥Use it very carefully. 
- It Runs onClick with No corfirmation
- dangerous-pull-this-branch.bat & dangerous-push-this-branch.bat has no `branch` specifed so **Please be carefull your current branch** and then use it.

## Prerequisite
- Check your remote urls. use `git remote -v`
    
- Add your `fetch` & `push` url links
   
- Add your urls 
~~~bash
git remote add gitlab https://gitlab.com/your-nam/repo
~~~   
~~~bash
git remote add github https://github.com/your-nam/repo
~~~ 

- Replace the origin with gitlab use
~~~bash
git branch -m <old-branch-name> <new-branch-name>
~~~
Example
~~~bash
git branch -m origin gitlab
~~~
💡 **Tip:** It is safe to use rename the origin to somthing else for automation of pull push.


## Dangerous Pull and Push Specific Branch bat file
On Specific branch case It might be like this
- pull.bat
```bat
@echo off 
git pull gitlab develop
pause
```
💡 **Tip:** using the `develop` branch for updated content. But you can use the `main` branch for stable contents.

- push.bat
```bat
@echo off 
git push github develop
pause
```

💡 **Tip:** using the `develop` branch is to not harm the `main` branch and to avoid the unnesary pushes.
