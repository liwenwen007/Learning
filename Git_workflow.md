# Git Workflows

[**reference**](https://www.atlassian.com/git/tutorials/comparing-workflows)

> Git offers a lot of flexibility in how users manage changes.
> When working with a team on a Git managed project, it’s important to make sure the team is all in agreement on how the flow of changes will be applied.
> To ensure the team is on the same page, an agreed upon Git workflow should be developed or selected.

## Centralized Workflow

* Characteristics
  * a central repository
  * only use _master_ branch

* Steps
  * Initialize the central repository on a server
    ```bash
    ssh user@host git init --bare /path/to/repo.git
    ```
  * Clone the central repository
    ```bash
    git clone ssh://user@host/path/to/repo.git
    ```
  * Make changes and commit
    ```base
    git pull # fetch the updated central commits and rebase their changes on top of them
    git pull --rebase origin master # During your working, someone else has pushed his work, then rebase is needed
    
    git status # View the state of the repo
    git add <some-file> # Stage a file
    git commit -m "details" # Commit a file</some-file>
    ```
  * Push new commits to central repository
    ```bash
    git push origin master
    ```

## Feature Branch Workflow

[**reference**](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)

multi-branches

> Git Feature Branch Workflow is branching model focused, meaning that it is a guiding framework for managing and creating branches. 

* Steps
  * match the latest version.
    ```bash
    # switch to master branch and reset the local copy of master
    git checkout master
    git fetch origin
    git reset --hard origin/master
    ```
  * Create a new-branch
    ```bash
    git checkout -b new-feature
    ```
  * Update, add, commit, and push changes
    ```bash
    git status
    git add <some-file>
    git commit -m "details"
    ```
  * Push feature branch to remote
    ```bash
    git push -u origin new-feature
    ```
  * Pull requests
    ```bash
    # push the feature branch to the central server and file a pull request asking to merge their additions into master. 
    git push
    ```
  * Merge the feature into the project finally
    ```bash
    git checkout master
    git pull
    git pull origin marys-feature
    git push
    ```
    git commit -m "details"`
    git commit -m "details"`
    git commit -m "details"
