# Version-Control-SCM
This about Source Code Management

I want to make 3 Branch:
1.  Production
2.  Trial
3.  Development

Why do i have to make it 3 ?
1.  Production  => Used for website that are currently running
2.  Trial       => For make merge branch Development into Production
3.  Development => Used to write code for CR or bug fixes

For init git folder:

    git init

For add all folder and file:

    git add .

And you mush commit first:
    
    // you cant use -m or -am, but if file updated code you should used -am
    // recomended use -am
    git commit -am "commit first" 

And than you remote git URL:

    git remote add origin <URL>
    
If you want make branch auto checkout:

    git branch -M <BRANCH NAME>

Check repository branch active:
    
    git branch

Push in GIT:

    git push -u origin <BRANCH NAME>

#MERGE
If you want merege 2 branch and allowed incoming files in DEV into TRIAL
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

How to check log commit:

    git log
    OR
    git log --al --decorate --online --graph

Making alias:
    
    alias graph ="git log --all --decorate --online --graph"
