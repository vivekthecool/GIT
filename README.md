1. If getting Long file path Error while cloning
    1. Fix in System level once:
        Open Git Bash as Administrator and run the command -> git config --system core.longpaths=true
	2. Fix for current Git Clone:
        git clone -c core.longpaths=true <repo-url>
		
2. Git commands:
    1. git init -> turns a directory into an empty Git repository. This is the first step in creating a repository. After running git init, adding and committing files/directories is possible.
        1. git init

	2. git add -> Adds files in the to the staging area for Git. Before a file is available to commit to a repository, the file needs to be added to the Git index (staging area). There are a few different ways to use git add, by adding entire directories, specific files, or all unstaged files.
		1. git add file_names...

	3. git commit -> Record the changes made to the files to a local repository. For easy reference, each commit has a unique ID. It’s best practice to include a message with each commit explaining the changes made in a commit. Adding a commit message helps to find a particular change or understanding the changes.
		1. git commit -m "commit message"

	4. git status -> This command returns the current state of the repository. git status will return the current working branch. If a file is in the staging area, but not committed, it shows with git status. Or, if there are no changes it’ll return nothing to commit, working directory clean.
        1. git status

	5. git config -> With Git, there are many configurations and settings possible. git config is how to assign these settings. Two important settings are user user.name and user.email. These values set what email address and name commits will be from on a local computer. With git config, a --global flag is used to write the settings to all repositories on a computer. Without a --global flag settings will only apply to the current repository that you are currently in.
		1. git config --global user.email "your_email"
		2. git config --global user.name "username"

    6. git branch -> To determine what branch the local repository is on, add a new branch, or delete a branch.
	    1. create new branch: git branch <branch_name>
		2. List all remote or local branches: git branch -a
		3. search specific branch in remote or local branches: git branch -a --list *<string>*
		4. Delete a branch: git branch -d <branch_name>

    7. git checkout -> To start working in a different branch, use git checkout to switch branches.
	    1. git checkout <branch_name>
		2. git checkout <file_name>

    8. git merge -> Integrate branches together. git merge combines the changes from one branch to another branch. For example, merge the changes made in a staging branch into the stable branch.
        1. git merge <branch_name>

    9. git remote -> To connect a local repository with a remote repository. A remote repository can have a name set to avoid having to remember the URL of the repository.
        1. Add remote repository: git remote <command> <remote_name> <remote_URL>
		2. List named remote repositories: git remote -v

    10. git clone -> To create a local working copy of an existing remote repository, use git clone to copy and download the repository to a computer. Cloning is the equivalent of git init when working with a remote repository. Git will create a directory locally with all files and repository history.
        1. git clone <remote_URL>
		
    11. git pull -> To get the latest version of a repository run git pull. This pulls the changes from the remote repository to the local computer.
        1. git pull <branch_name> <remote_URL/remote_name>
		2. git pull 
		
    12. git push -> Sends local commits to the remote repository. git push requires two parameters: the remote repository and the branch that the push is for.
        1. git push <remote_URL/remote_name> <branch>
		2. Push all local branches to remote repository: git push —all
		3. git push
		
    13. git stash -> To save changes made when they’re not in a state to commit them to a repository. This will store the work and give a clean working directory. For instance, when working on a new feature that’s not complete, but an urgent bug needs attention.
        1. Store current work with untracked files: git stash -u
		2. Bring stashed work back to the working directory: git stash pop
		
    14. git log -> To show the chronological commit history for a repository. This helps give context and history for a repository. git log is available immediately on a recently cloned repository to see history.
        1. Show entire git log: git log
		2. Show git log with date pameters: git log --<after/before/since/until>=<date>
		3. Show git log based on commit author: git log --<author>="Author Name"
		
    15. git rm -> Remove files or directories from the working index (staging area). With git rm, there are two options to keep in mind: force and cached. Running the command with force deletes the file. The cached command removes the file from the working index. When removing an entire directory, a recursive command is necessary.
        1. To remove a file from the working index (cached): git rm --cached <file name>
		2. To delete a file (force): git rm -f <file name>
		3. To remove an entire directory from the working index (cached): git rm -r --cached <directory name>
		4. To delete an entire directory (force): git rm -r -f <file name>
		
    16. git fetch
	
    17. git restore --staged <file>