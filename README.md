# Version-Control-SCM <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px">
This about Source Code Management

#### LIST
- [Introduction 👻](#introduction-)
    - This all about all merge 2 way, with strategy "theirs", merge by allow unreleated history, reset merge
        - [Merge 👻](#merge-)
- [Log 👻](#log-)
- [Alias 👻](#alias-)
- [Delete 👻](#delete-)
- [Show 👻](#show-)
- [Set Global User 👻](#set-global-user-)
- [Clone 👻](#clone-)
- [Personal Access Token 👻](#personal-access-token-)
- [Referance 👻](#referance-)

#### INTRODUCTION 👻
if your place or company not yet used git and than you should to make 3 Branch for compare all source code:
1.  ![](https://img.shields.io/badge/-Production-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=2bbc8a)
2.  ![](https://img.shields.io/badge/Stag-Trial-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=2ba9bc)
3.  ![](https://img.shields.io/badge/-Development-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=bc2b2b)

Why do i have to make it 3 ?
1.  ![](https://img.shields.io/badge/-Production-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=2bbc8a) => Used for website that are currently running
2.  ![](https://img.shields.io/badge/Stag-Trial-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=2ba9bc) => For make merge branch Development into Production
3.  ![](https://img.shields.io/badge/-Development-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=bc2b2b) => Used to write code for CR or bug fixes

For init git folder:

    git init

For add all folder and file:

    // remove cache git rm -rf --cached .
    git add .

And you mush commit first:
    
    // you cant use -m or -am, but if file updated code you should used -am
    // recomended use -am
    git commit -am "commit first" 

And than you remote git URL:

    git remote add origin <URL>

Case beacause you already remote branch:
    
    fatal: remote origin already exists.
    
You should set remote, follow this tag:

    git remote set-url origin <URL>

If you want make branch auto checkout:

    git branch -M <BRANCH NAME>

Check repository branch active:
    
    git branch

Push in GIT:

    git push -u origin <BRANCH NAME>

#### MERGE 👻
### OPTION 1 MERGE
If you want merege 2 branch and allowed incoming files in DEV into TRIAL <br>
<br>
Checkout Branch MASTER OR TRIAL OR STAGGING OR CENTER:

    checkout <BRANCH MASTER NAME EXAMPLE: trial>

And MERGE branch destination:

    git merge -X theris <BRANCH ANOTHER NAME EXAMPLE: dev>

If this case 
    
    merge: dev - not something we can merge

solve: you don't have branch dev.
if you want all branch or you want spesific branch:

    git fetch origin <BRANCH NAME EXAMPLE: dev>

The error is resolved by toggling the "allow-unrelated-histories" switch. After a git pull or git merge command, add the following tag:

    fatal: refusing to merge unrelated histories

Use anything with --allow-unrelated-histories:

    git pull origin <BRANCH NAME> --allow-unrelated-histories
    OR
    git push -u origin <BRANCH NAME> --allow-unrelated-histories
    OR
    git merge -X theirs <BRANCH ANOTHER NAME EXAMPLE: dev> --allow-unrelated-histories
    
Remember USED THIS:

    < --allow-unrelated-histories >
    
Check branch MERGED:
    
    git branch --merged

![image](https://user-images.githubusercontent.com/77251566/139561661-2b62076c-b9cd-4f84-a977-b64c5cfba81a.png)

### OPTION 2 MERGE
This clone all branch:
    
    git clone <URL>

Check all branch:
    
    git branch -a or git branch -r

Checkout branch first what you need, for update branch:
    
    git checkout <branch name>

Merge:
    
    <example position remote in branch master>
    git merge <target branch name>

And if the conflict and you see it's not too much trouble with the conflict you can reset it first and merge the dominant auto update in the incoming branch/them.
This sample conflict and not too much trouble:
![image](https://user-images.githubusercontent.com/77251566/147038638-7de51fa3-b4b1-4f04-8141-73d24a62dd21.png)

Reset MERGE:
    
    git reset --merge
    
Merge strategy theirs:
    
    git merge --strategy-option theirs

#### LOG 👻
How to check log commit:

    git log
    OR
    git log --all --decorate --oneline --graph

#### ALIAS 👻
Making alias:
    
    alias graph ="git log --all --decorate --online --graph"

#### DELETE 👻
Delete local branch:
    
    git branch -d <BRANCH NAME>
    OR
    git branch -D <BRANCH NAME>
    
#### SHOW 👻
Show existing remote url:
    
    git remote show origin
    OR
    git remote -v

#### SET GLOBAL USER 👻
How to set and check user:

    Set:
    git config –global user.email “you@example.com” 
    git config –global user.name “your name”
    
    Check:
    git config –global user.email 
    git config –global user.name
    
#### CLONE 👻
How to any clone all branch all single:

    Clone all branch:
    git clone <url>
    
    Clone single branch:
    # clone only the remote primary HEAD (default: origin/master)
    git clone <url> --branch [BRANCH_NAME (IF NOT USE THAN USE DEFAULT BRANCH)] --single-branch
    
    Clone single branch folder:
    git clone <url> --branch <branch> --single-branch [<folder>]
    
#### PERSONAL ACCESS TOKEN 👻
How use personal access token without password git:

    Login Git -> Setting -> Developer Setting -> Personal Access Tokens
    
#### REFERANCE 👻
[Documentation](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories) <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px">
