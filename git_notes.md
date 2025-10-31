# Git commands and usage

- ``git fetch origin``
- ``git reset --hard origin/Pre-Production``				*to pull the branch and overwrite the local changes*
- ``git status`` 																	  ***to view the files which have changes.***
- ``git add file_path/file_name``  								  ***to add file(s) which have changes***
- ``git commit -m "message for commit"`` 						***to commit the changes)***
- ``git push``																		***to push the changes at repository***

To merge Pre-Production with Production
---------------------------------------
- ``git checkout Production``
- ``git pull origin Production``
- ``git merge Pre-Production``
- ``git push origin Production``

- ``git branch -d branch_name`` 			***to delete a branch***
- ``git branch -D branch_name``			***to delete a branch forcefully***

- ``git stash``        ***to locally save the changes to switch to another branch, for example one at pre-production branch and want temporarily switch to production branch***  
- ``git switch Production``  ***to switch to a branch named Production***
- ``git stash pop``  ***After switch back to previous branch for example, pre-production, use ```git stash pop``` to restore the local changes*** 

# Create a local branch "Production" from remote
git checkout -b Production origin/Production
git checkout -b Pre-Production origin/Pre-Production

git diff --name-status origin/Pre-Production..origin/Production  -- to see the files which have difference in both branches
git diff origin/Pre-Production..origin/Production                -- to see the detail of differences
git diff --name-status																					 -- to show only the name of files which are modified.
git diff file_name																							 -- To see difference of given file

git restore -s origin/Pre-Production --  public/elements/alert-configuration/view-edit-pattern-matching.html
git restore -s origin/Pre-Production --  server/joiSchema.js


# Merge Pre-Production into Production
git merge origin/Pre-Production

git checkout origin/Production -- Configurations.py		-- revert just Configurations.py back to Production’s version
git checkout origin/Pre-Production -- server/joiSchema.js

git add Configurations.py
git commit   # finish merge commit
git push origin Production

git update-index --assume-unchanged <file_path>   	-- to ignore the changes of a file and keep this file in repo
git update-index --no-assume-unchanged <file_path>	-- again consider the changes of the file

git update-index --skip-worktree Configurations.py	--to ignore the changes of a file and keep this file in repo
git update-index --no-skip-worktree Configurations.py   --Ask Git - to consider the changes of the file


git restore Configurations.py		-- to overwrite the local changes
git restore .				-- Discard changes in all files

git fetch origin
git reset --hard origin/Pre-Production	-- Hard reset everything (⚠️ destroys local changes)

git fetch origin														
git reset --hard origin/Pre-Production		-- to over write local changes forcefully

