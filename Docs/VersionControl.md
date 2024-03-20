# Source Code Version Control Tools
## Introduction
Source control is vital for maintaining a standardized working environment, whether collaborating within a team or working solo. Ensuring that the source code remains consistent across all devices is crucial to ensure functionality. This includes maintaining all dependencies in a usable state to prevent code from breaking due to changes in dependencies. Moreover, using version control enables the preservation of previous code states, facilitating quick fixes by reverting to earlier working versions

## Github
This specific project uses **Github** to deal with all source control. There are many benefits in using Github for this purpose, including easy implementation from VSCode. Github can be used directly from the UI of VSCode, making it very easy to use and navigate. Additionally, Github actions provides a lot of utility in creating developement pipelines. For more information the Github docs can be found [here](https://docs.github.com/en).

### Repository Structure
* [.devcontainer](../.devcontainer)
    * This is the location of the flutter dev container files. This allows for a standard developer environment, eliminating the *it works on my machine* problem.
* [.github](../.github/)
    * This contains the files responsible for dealing with github. This contains things such as github workflows that activate when anything is pushed to the repository.
* [Docs](./)
    * This folder contains all documentation for the project.
* [app](../app)
    *This contains all of the wokring files for the flutter app. This is where all work done within the container should go to.
### Common Commands and Usage
* git clone: Clone a repository into a new directory.
    *       git clone <repository_url>

* git init: Initialize a new Git repository.
    *       git init

* git add: Add file contents to the index (staging area).
    *       git add <file_name>
* git commit: Record changes to the repository.
    *       git commit -m "Commit message"
* git push: Update remote refs along with associated objects.
    *       git push <remote_name> <branch_name>
* git pull: Fetch from and integrate with another repository or a local branch.
    *       git pull <remote_name> <branch_name>
* git fetch: Download objects and refs from another repository.
    *       git fetch <remote_name>
* git branch: List, create, or delete branches.
    *       git branch
            git branch <branch_name>
            git branch -d <branch_name>

* git checkout: Switch branches or restore working tree files.
    *       git checkout <branch_name>
            git checkout -b <new_branch_name>

* git merge: Join two or more development histories together.
    *       git merge <branch_name>

* git status: Show the working tree status.
    *       git status

* git log: Show commit logs.
    *       git log
* git remote: Manage set of tracked repositories.
    *       git remote add <remote_name> <repository_url>
            git remote -v
* git rm: Remove files from the working tree and from the index.
    *       git rm <file_name>
* git mv: Move or rename a file, a directory, or a symlink.
    *       git mv <source> <destination>
## Collaboration Features
  GitHub offers numerous benefits for collaboration in software development projects. Firstly, it provides a centralized platform for version control, allowing team members to track changes, collaborate on code, and manage project history efficiently. GitHub's pull request feature facilitates code review processes, enabling developers to suggest changes, discuss implementation details, and ensure code quality before merging into the main branch. Additionally, GitHub's issue tracker streamlines communication by providing a space to report bugs, discuss feature requests, and organize tasks, fostering transparency and accountability within the team. Furthermore, GitHub's integration with various development tools and services enhances workflow automation, making tasks such as continuous integration, deployment, and project management seamless and efficient. Overall, GitHub significantly enhances collaboration by offering a robust set of features tailored to the needs of modern software development teams.
## Challenges and Solutions
* Check the issues page on github found [here](https://github.com/Zaxbys-Toast/CSC325DevContainer/issues)
## Conclusion
* Github provides this project with a lot of utility in maintaining a standard devlopement environment, and allows for near seamless collaboration.
