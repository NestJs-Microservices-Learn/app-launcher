## Dev

1. Clone the repository
2. Create a .env file based on the .env.template
3. Run the command `docker compose up --build`

### Steps to create Git Submodules

1. Create a new repository on GitHub
2. Clone the repository to your local machine
3. Add the submodule, where `repository_url` is the URL of the repository and `directory_name` is the name of the folder where you want the submodule to be saved (the folder should not exist in the project)

```
git submodule add <repository_url> <directory_name>
```

4. Add the changes to the repository (git add, git commit, git push)
   Example:

```
git add .cambios al repositorio (git add, git commit, git push)
git commit -m "Add submodule"
git push
```

5. Initialize and update submodules: when someone clones the repository for the first time, they should run the following command to initialize and update the submodules
   it push

```
git submodule update --init --recursive
```

6. To update the references of the submodules

```
git submodule update --remote
```

## Important

If you are working in the repository that has submodules, **first update and push** in the submodule and **then** in the main repository.

If done in reverse, the submodule references in the main repository will be lost and conflicts will need to be resolved.

# Prod

1. Clone the repository
2. Create a .env file based on the .env.template
3. Run the command

````
docker compose -f docker-compose.prod.yml build
```
````
