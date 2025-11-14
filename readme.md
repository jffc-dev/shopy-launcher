### Dev
1. Clone repo
2. Create .env file based on .env.template
3. Run `git submodule update --init --recursive`
4. Run `docker compose up --build`


### Steps to create Git Submodules


1. Create new GitHub repo
2. Clone repo locally
3. Add the submodule, where `repository_url` is the url of the repo and `directory_name` is the name of the folder where the submodule will be stored (it shouldn't exist in the project)
```
git submodule add <repository_url> <directory_name>
```
4. Add the chages (git add, git commit, git push)
Ex:
```
git add .
git commit -m "Add submodule"
git push
```
5. Initialize and update Submodules, When someone clones the repository for the first time, they must run the following command to initialize and update the submodules:
```
git submodule update --init --recursive
```
6. To update the submodule references
```
git submodule update --remote
```


## Important
If you are working inside the repository that contains the submodules, you must first update and push in the submodule, and then in the main repository.

If you do it the other way around, the submodule references in the main repository will be lost, and you’ll have to resolve conflicts.
