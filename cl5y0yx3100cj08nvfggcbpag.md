# Get Start with Git and GitHub

-  Git

> Git is a free, open-source version control software.

- Then what is github?

> Github is a git repository system where we host our files.

- Let's install git

> All the installation process based on windows in this post

Go to <https://git-scm.com/download/win>

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658577761473/vqhlZgly4.png align="left")


Download 64 or 32 bit version acording to your system.

**And** install them with default settings.

- Now open terminal in project folder on your IDE or in Windows Terminal
>Powershell recommended

type:

```
git --version

```
If it shows something like this then all looks good
```
git version 2.31.1.windows.1
```

- Now create a repository on GitHub
    - Login into github or signup for first time

>add `user name` and `email` on your git by using this command:

```
git config --global user.name "your name"
git config --global user.email "youremail@example.com"
```
   - Get back to github

>click on plus icon top-right of page and hit on `New Repository`

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658579337030/A8seUwSdv.png align="left")


>give it a name and click `Create Repository`


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658579629405/5ljxDJsvn.png align="left")

> Copy the repository path


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658581636126/V1b5Hne7v.png align="left")

- In terminal use these command:

> First initialize git into project

```
git init
```
> Check files are listed

```
git status
```

> Commit the code files

```
git commit -m "initial commit"
```
 > Add files to main branch

```
git branch -M main
```

>Now add your remote repository link

```
git remote add origin https://github.com/yourName/project-name.git
```

> With this final command push your code form local repository to github

```
git push origin master
```






