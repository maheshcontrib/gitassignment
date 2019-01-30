#### Getting hands-on using Git Basics 
1. Signup to GitHub using you Gmail ID
2. Create a repo with name `ncrwork`
3. Set basic global configuration
    ```bash
    touch main.c
    ```
4. Clone the repo
    ```bash
    git clone https://github.com/maheshcontrib/ncrwork
    ```
5. Create a folder `arith`. Inside the folder create file `main.c`.
    ```bash
    touch main.c
    ```
6. See the status of repo
    ```bash
    git status
    ```
7. Tell git to stage the file and keep it tracked
    ```bash
    git add main.c
    ```
8. Check status again. Note the difference.
9. Commit the change
    ```bash
    git commit -m "Added main file for the project"
    ```
10. Check status again. Note the difference.
11. Have a look at the repo on the web browser. It should be empty.
```bash
    git status
```
12. Push the commits to the remote repo
```bash
    git push
```
13. Have a look at the repo on the web browser. It should contain `main.c`.

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
6. Check status of repo
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

#### Additional assignment
1. Add a new feature for implementing subtract functionality
