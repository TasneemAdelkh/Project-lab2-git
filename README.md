# Project-lab2-git

- creating local repo and pulling remote repo 
    - git init
    -  git remote add origin git@github.com:TasneemAdelkh/Project-lab2-git.git
    -  git pull origin main

- creating 2 branches (dev & test) and add files to each
    - creating dev branch
        - git checkout -b dev
        - vim app.py
        - git add .
        - git commit -m "create app.py having username"
    - creating test bran
        - git checkout main
        - git branch test
        - git checkout test
        - vim test.py
        - git add .
        -  git commit -m "create test.py file"
        -  git switch main
    - pushing branches to remote repo
        -  git push origin --branches

- merge both branches to main and push it to remote repo
    -  git merge dev
    - git merge test
    - git push origin main
- deleting both branches locally and remotely
    -  git branch -d dev
    - git branch -d test
    -  git push origin :dev
    - git push origin :test

- creating a new branch and make in it changes without commiting and checking out other branch
    - git checkout -b "feature/addition"
    - vim app.py
    - git stash
    - git checkout main
    - vim test.py
    - git commit -am "add comment to test.py"
    - git checkout feature/addition
    - git stash pop
    - git commit -am "add addition function"
    - git switch main
    - git merge feature/addition
    - git branch -d feature/addition

- adding an annotated tag
    - git tag -a v1.7 -m "version 1.7"
    - git push origin v1.7
    - git push origin main

- listing the existing tags
    - git tag

- deleting tag locally and remotely
    - git tag -d v1.7
    - git push origin :v1.7

- adding an image to the README file

![random nature photo](images/nature.jpg)
