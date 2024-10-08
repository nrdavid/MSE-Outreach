# MSE-Outreach
Materials Science and Engineering Outreach at The University of Michigan

## Installation Instructions

Ensure that conda is installed. If not, see installation instructions [here](https://conda.io/projects/conda/en/latest/user-guide/install/index.html).
```sh
conda --version
```

Nagivate to the folder you want to work out of and clone the repository:
```sh
git clone https://github.com/nrdavid/MSE-Outreach.git
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

First, checkout a branch for your changes. You can call this whatever you want, preferably something relevant to what section you're editing. For example, if I (Gillian) am updating the battery_lab section, I might call my branch "GJ_battery"

```sh
git checkout -b <BRANCH_NAME>
```
Set your upstream for the branch

```sh
git branch --set-upstream-to=origin/<BRANCH_NAME>  <BRANCH_NAME>
```
Make your wonderful changes however you see fit. Now, push your changes. Please commit your edits with a meaningful message! 

```sh
git add .
git commmit -m "I added X, Y, and Z to the <SECTION> section"
git push -d origin <BRANCH_NAME>
```

then pull the latest changes from main and rebase your changes to `main`

```sh
git checkout main 
git pull
```
```sh
git checkout <BRANCH_NAME>
git rebase main <BRANCH_NAME>
```


Once your branch has been used to commit changes, you can delete it

```sh
git branch -D <BRANCH_NAME>
```

NOTE -  make sure you are regularly pulling changes from `main` to keep your local repository updated!! 