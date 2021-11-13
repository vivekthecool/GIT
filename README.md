1. If getting Long file path Error while cloning
	Fix in System level once:
		Open Git Bash as Administrator and run below line- 
			git config --system core.longpaths=true
	Fix for current Git Clone:
		git clone -c core.longpaths=true <repo-url>
		
2. Git commands:
	git fetch
	git pull
	git checkout <branch_name>
	git checkout <file_name>      ----- to replace from the origin
	git add file_name...
	git rm file_name
	git commit -m "commit message"
	git push
	git branch -a --list *any keyword of the branch*
	git status
	git config --global user.email "vivekjavadvlpr@gmail.com"
	git config --global user.name "vivekthecool"
	git restore --staged <file>...            -------- to unstage
