echo "# git-test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/makgith/git-test.git
git push -u origin main

git clone
git push
git pull

git push --set-upstream origin branch_2 - sets upstream 'origin' for local branch as branch_2

git reflog -  keep track of when the tips of branches and other references in the local repository are modified.