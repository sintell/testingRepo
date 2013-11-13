testingRepo
===========
* git clone --no-hardlinks frontik testing
* cd testing/
* git filter-branch --subdirectory-filter frontik/testing HEAD -- --all
* git reset --hard
* git gc --aggressive
* git prune
* cd ../frontik/
* git filter-branch --tree-filter "rm -rf frontik/testing" --prune-empty HEAD
* git remote remove origin
* git remote add origin git@github.com:sintell/frontikRepo.git
* git push origin master
* cd ../testing/
* git remote remove origin 
* git remote add origin git@github.com:sintell/testingRepo.git
* git push origin master
