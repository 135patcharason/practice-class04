[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/3ACHtEIJ)
# INT142 Software Development Tools
## Class 02 Working on local repository first

### Exercise 1

In this class exercise, you will initialize empty git repository on your local machine first. After working on your class02 exercise 1 work, you will push your work to **empty** remote repository on **your github account**.

### Instructions
1. Move to your class directory  
    ```bash
    $ cd Documents/<your-github-id>
    ```

2. Create a new directory for this exercise  
    ```bash 
    $ mkdir class02-ex1
    ```

3. Move to this exercise directory  
    ```bash
    $ cd class02-ex1
    ```

4. Initialize empty repository and check that it is initialized  
    ```bash
    $ git init
    
    $ git status
    ```

5. Open VS Code  
    ```bash
    $ code .
    ```

6. Create a new file `index.html` and copy the following html code and save the file.  
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Class 02 Exercise 1</title>
        <style>
            body { font-family: sans-serif; text-align: center; margin-top: 50px; }
            .container { border: 1px solid #ccc; padding: 20px; border-radius: 8px; max-width: 600px; margin: 0 auto; }
        </style>
    </head>
    <body>

        <div class="container">
            <h1>INT142 Software Development Tools</h1>
            <h1 id="class">Class 02 Exercise 1</h1>
            <h2 id="student-name">Replace This With Your Name</h2>
            
            <p>This page was created locally and pushed to GitHub Classroom.</p>
        </div>

    </body>
    </html>
    ```

7. Add `index.html` to the staging area  
    ```bash
    $ git add .
    ```

8. Commit your work  
    ```bash
    $ git commit -m "Initial commit - add index.html"
    ```

9. View commit history  
    ```bash
    $ git log
    ```

10. Change commit author name and email as follows:  
    ```bash
    $ git config --local user.name "<Firstname Surname> (INT142-class02)"
    
    $ git config --local user.email <your-private-github-email>
    ```

    Amend previous commit without changing the commit message:  
    ```bash
    $ git commit --amend --reset-author --no-edit
    ```

    Amend the commit message:  
    ```bash
    $ git commit --amend -m "<new message>"
    ```

    Ensure that your commit author and message are correct before proceeding to the next step.

11. Rename default branch to `main` (needed on Windows only)  
    ```bash
    $ git branch -M main
    ```

12. Create new repository on your personal GitHub account with the name `INT142-class02`. Set it to `private`.

13. Add remote repository  
    ```bash
    $ git remote add origin https://github.com/<your-github-username>/INT142-class02.git
    ```

14. View remote setting
    ```bash
    $ git remote -v
    ```

    Ensure that the url is correct. If not, use the following command to set url.
    ```bash
    $ git remote set-url origin <new-url>
    ```    

15. Make sure that the remote url is correct by fetching from remote repository  
    ```bash
    $ git fetch
    ```

16. Check the current local repository status.  
    ```bash
    $ git status
    On branch main
    nothing to commit, working tree clean
    ```

17. Push your work to the remote repository  
    ```bash
    $ git push -u origin main
    ```
    You should have successfully push `index.html` to your GitHub repository.

18. Update `index.html`, replace `Replace This With Your Name` with your fullname.

19. Add the updated `index.html` to the staging area and commit with the message `Update index.html with student name`

20. Push the update to your remote repository

---

### Exercise 2

In this class exercise, you will start working on your local repository first as in Exercise 1. However, you will link this to GitHub classroom repository which is **not empty**.



### Instructions
1. Work on a new directory called `class02-ex2` under `Documents/<your-github-id>`

2. Create a new file `index.html` and copy the following html code and save the file.  
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Class 02 Exercise 2</title>
        <style>
            body { font-family: sans-serif; text-align: center; margin-top: 50px; }
            .container { border: 1px solid #ccc; padding: 20px; border-radius: 8px; max-width: 600px; margin: 0 auto; }
        </style>
    </head>
    <body>

        <div class="container">
            <h1>INT142 Software Development Tools</h1>
            <h1 id="class">Class 02 Exercise 2</h1>
            <h2 id="student-name">Replace This With Your Name</h2>
            
            <p>This page was created locally and pushed to GitHub Classroom.</p>
        </div>

    </body>
    </html>
    ```

3. Initialize local repository  

4. Configure `user.name` and `user.email` as in Exercise 1. Check that it is correct.

5. Rename default branch to `main` (needed on Windows only)  

6. Add `index.html` to the staging area  

7. Commit your work. Check commit history and make sure that it is correct. If not, amend the commit meta-data.

8. Add remote repository `https://github.com/IT-BANGMOD-INT142-2025/class02-<your-github-username>.git`. Check that the configuration is correct.   

9. (Not normally needed) Manually configure upstream.
    ```bash
    $ git branch --set-upstream-to=origin/main main
    branch 'main' set up to track 'origin/main'.
    
    $ git branch -vv
    * main b54bb45 [origin/main: ahead 1, behind 2] Initial commit - add index.html
    ```

10. Fetch meta-data from the remote repository  
    ```bash
    $ git fetch
    remote: Enumerating objects: 10, done.
    remote: Counting objects: 100% (10/10), done.
    remote: Compressing objects: 100% (4/4), done.
    Unpacking objects: 100% (10/10), 3.54 KiB | 725.00 KiB/s, done.
    remote: Total 10 (delta 1), reused 3 (delta 0), pack-reused 0 (from 0)
    From github-olarn-ad:IT-BANGMOD-INT142-2025/class02-olarnr-ad-sit
    * [new branch]      main       -> origin/main
    ```

11. Check the current local repository status.  
    ```bash
    $ git status
    On branch main
    Your branch and 'origin/main' have diverged,
    and have 1 and 2 different commits each, respectively.
        (use "git pull" to merge the remote branch into yours)

    nothing to commit, working tree clean
    ```

12. Push your work to the remote repository. Since there is a commit on remote repository and local and remote repository have diverged, there will be error.
    ```bash
    $ git push -u origin main
     ! [rejected]        main -> main (non-fast-forward)
    error: failed to push some refs to 'github-olarn-ad:IT-BANGMOD-INT142-2025/class02-olarnr-ad-sit.git'
    hint: Updates were rejected because the tip of your current branch is behind
    hint: its remote counterpart. Integrate the remote changes (e.g.
    hint: 'git pull ...') before pushing again.
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.
    ```

13. You need merge commit on remote repository to your local repository before you can push your work to the remote repository.
    ```bash
    $ git pull origin main --allow-unrelated-histories --no-rebase --no-edit
    From github-olarn-ad:IT-BANGMOD-INT142-2025/class02-olarnr-ad-sit
    * branch            main       -> FETCH_HEAD
    Merge made by the 'ort' strategy.
    .github/workflows/classroom.yml | 135 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
    1 file changed, 135 insertions(+)
    create mode 100644 .github/workflows/classroom.yml
    ```

    `--allow-unrelated-histories` since the two commits do not have common ancestor, needed this to merge  
    `--no-rebase` use merge, not rebase   
    `--no-edit` use auto-generated merge message

14. View commit history
    ```bash
    $ git log

    $ git log --graph --oneline
    *   bd45a16 (HEAD -> main) Merge branch 'main' of github-olarn-ad:IT-BANGMOD-INT142-2025/class02-olarnr-ad-sit
    |\  
    | * 68f56e2 (origin/main) Initial commit
    * b54bb45 Initial commit - add index.html
    ```

15. Push to remote repository again
    ```bash
    $ git push
    Enumerating objects: 6, done.
    Counting objects: 100% (6/6), done.
    Delta compression using up to 10 threads
    Compressing objects: 100% (4/4), done.
    Writing objects: 100% (5/5), 986 bytes | 986.00 KiB/s, done.
    Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (1/1), done.
    To github-olarn-ad:IT-BANGMOD-INT142-2025/class02-olarnr-ad-sit.git
    68f56e2..bd45a16  main -> main
    ```

16. View your grading on GitHub. You should get 70/100 points.

17. Make changes and commit/push again to get 100 points.
