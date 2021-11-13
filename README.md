1. If getting Long file path Error while cloning
    1. Fix in System level once:
        Open Git Bash as Administrator and run the command -> git config --system core.longpaths=true
	2. Fix for current Git Clone:
        git clone -c core.longpaths=true <repo-url>
		
2. Git commands:
    1. git fetch
    2. git pull
    3. git checkout <branch_name>
    4. git checkout <file_name>      ----- to replace from the origin
    5. git add file_name...
    6. git rm file_name
    7. git commit -m "commit message"
    8. git push
    9. git branch -a --list *any keyword of the branch*
    10. git status
    11. git config --global user.email "your_email"
    12. git config --global user.name "username"
    13. git restore --staged <file>...            -------- to unstage
