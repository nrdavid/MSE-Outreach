# MSE-Outreach
Materials Science and Engineering Outreach at The University of Michigan

## Installation Instructions

Ensure that conda is installed. If not, see installation instructions [here](https://conda.io/projects/conda/en/latest/user-guide/install/index.html).
```sh
conda --version
```

Firstly, you'll want to create your own fork of the main repository, which will be where you will make your edits. 

Nagivate to the folder you want to work out of on your computer and clone your forked repository:
```sh
git clone https://github.com/<your_username>/MSE-Outreach.git
cd MSE-outreach
```

Create an environment from the environment.yml file (this ensures that all your dependencies will be correct)
```sh
conda env create -f environment.yml
conda activate MSE-outreach
```

The server can be locally run using
```sh
mkdocs build
mkdocs serve
```

Copy the host ip into any browser to see updates to website in real-time!

## How to contribute

Firstly, set your upstream branch to the main remote repository

```sh
git remote add upstream https://github.com/nrdavid/MSE-Outreach.git
```
This sets your `upstream` branch to the original repository, and your `origin` branch should be your forked repo. Verify your upstream and origin branches are correctly configured, you can run `git remote -v`
In your local machine, checkout a branch from your forked repo for your changes. You can call this whatever you want, preferably something relevant to what section you're editing. For example, if I (Gillian) am updating the battery_lab section, I might call my branch "GJ_battery"

```sh
git checkout -b <BRANCH_NAME>
```
Every time you make edits, it is a good idea to ensure your fork is up-to-date with the upstream repo BEFORE you make changes. To update your fork, run. Depending on your OS and git version, your 'main' branch may also be called 'master' If you get an error saying the branch name main doesnt exist, try running instead with master. 

```sh
git checkout main
git pull upstream main
git push origin main
```
Now, make your wonderful changes however you see fit. When you are finished, add, commit, and push your branch to the remote repository. Please commit with a descriptive message explaining your changes! 

```sh
git add .
git commit -m "I added X, Y, and Z to the <SECTION> section on file <FILENAME>"
git push origin <BRANCH_NAME>
```

Now, go to your branch on your forked repo on github.com. Create a pull request, add a meaningful description and title, and wait for the admin to approve your pull request. This will merge your changes with the main repo! 

NOTE - Make sure you frequently update your fork from the upstream `main` branch before and after you make changes to keep your local repo updated!!

```sh
git checkout main 
git pull upstream main
git push origin master
```

If you encounter any merge conflicts while pulling information, run the following, which pulls the latest changes from main and rebases your changes to `main`
```sh
git checkout <BRANCH_NAME>
git rebase main <BRANCH_NAME>
```

Once your branch has been used to commit changes, you can delete it

```sh
git branch -D <BRANCH_NAME>
```
It is good practice to make a new branch every time you make changes, and delete it afterwards. 