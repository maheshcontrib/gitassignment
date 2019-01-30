#### Git Assignment 
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
