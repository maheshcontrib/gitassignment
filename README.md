#### Getting hands-on using Git Basics 
1. Signup to GitHub using you Gmail ID
2. Create a repo with name `ncrwork`
3. Set basic global configuration for username and email ID
    ```bash
    git config --global user.name “Mahesh Patil”
    git config --global user.email “maheshcontrib@gmail.com”
    ```
    > Replace with your `name` and `email`
4. Set configuration for preety colors on the console
    ```bash
    git config --global color.ui auto
    ```
5. Clone the repo
    ```bash
    git clone https://github.com/maheshcontrib/ncrwork
    ```
6. Create a folder `arith`. Inside the folder create file `main.c`.
    ```bash
    touch main.c
    ```
7. See the status of repo
    ```bash
    git status
    ```
8. Tell git to stage the file and keep it tracked
    ```bash
    git add main.c
    ```
9. Check status again. Note the difference.
10. Commit the change
    ```bash
    git commit -m "Added main file for the project"
    ```
11. Check status again. Note the difference.
12. Have a look at the repo on the web browser. It should be empty.
```bash
    git status
```
13. Push the commits to the remote repo
```bash
    git push
```
14. Have a look at the repo on the web browser. It should contain `main.c`.

#### Add new feature to the code for adding two integers.
1. Find how many branches exists
    ```bash
        git branch
    ```
2. Create a new branch for feature. We will call it as `addfeature`
    ```bash
        git branch addfeature
    ```
3. Again find how many branches exists. This time it should be two `master` and `addfeature`
    ```bash
        git branch
    ```
4. Checkout the `addfeature` branch
    ```bash
        git checkout addfeature
    ``` 
5. Create new file `add.c` and implement the functionality
    ```bash
        touch add.c
    ```
    > Contents of add.c
    ```C
    int add(int a, int b) 
    {
        int sum=0;
        sum = a+b;
        return sum;
    }
    ```
6. Check status of repo. Note your observations.
    ```bash
        git status
    ```
7. Add the file `add.c` to staging so that it is tracked
    ```bash
        git add add.c
    ```
8. Commit the changes 
    ```bash
        git commit -m "Added functionality for add feature"
    ```
9. Checkout `master` repo. See the contents of the directory and note changes. `add.c` file would be missing, because it is in `addfeature` repo.
    ```bash
        git checkout master
    ```
10. Let's merge the `addfeature` branch `master` branch
    ```bash
        git merge addfeature
    ```
11. You will now see that `add.c` has been merged into `master` branch 
12. You can now push the new feature to remote repo
    ```bash
        git push
    ```
13. Have a look at the repo on the web browser. It should contain `main.c` and `add.c` both of it.
14. Can you trace the changes in the project. Yes, get hold of all the commit messages by using the following command
    ```bash
        git log
    ```
    > Tip: Use  `q` to exit the log in case it spans multiple pages

#### How to retrieve old changes
1. List the contents of the directory for master brach `HEAD`
    ```bash
    ls # Linux
    dir # Windows
    ```
2. Note the hash in the output of `git log ` command for the snapshot of source code you want to retrieve. The use the following command.
    ```bash
    git checkout *hash*
    ```
    > `hash` is hash of the snapshot you want to retrieve
3. Now have a look at the source code and see the changes as opposed to the `master` branch

#### Additional assignment
1. Add a new feature for implementing subtract functionality
2. Give your friend an access to your repo. Let her/him add new features of multiplication and push it to the repo. How do you get that feature replicated in your local repo.
    > Use following command

    ```bash
        git pull
    ```

#### Tips
>Use following command to get rid of frequent authentication prompts

```bash
git config credential.helper store
```
