### Introduction sequence
####level 1: Introduction to git
<pre><code>- git commit
- git commit </code></pre>

level 2: Branching in git
- git branch bugFix
- git checkout bugFix

level 3: 
- git checkout -b bugFix
- git commit
- git checkuout master
- git commit
- git merge bugFix

level 4: rebasing
- git checkout -b bugFix
- git commit
- git checkout master
- git commit
- git checkout bugFix
- git rebase master

------------------------------
Ramping up
level 1: Detach HEAD
- git checkout C4

level 2: Relative Refs
- git checkout C4^

level 3: Relative Refs 2
- git checkout HEAD^
- git branch -f master C6
- git branch -f bugFix C0

level 4: Reversing changes in git
- git rebase HEAD^
- git checkout pushed
- git revert HEAD

-------------------------------
Moving work around
level 1: cherry pick intro
- git cherry-pick C3 C4 C7

level 2: Interactive rebase intro
- git rebase -i HEAD~4

--------------------------------
A mixed bag
level 1: Grabbing just one commit 
- git checkout master
- git cherry-pick C4

level 2: Juggling commits
- git rebase -i HEAD~2 (reorder the commits C3 followed by C2)
- git commit --amend
- git rebase -i HEAD~2 (reorder the commits C2'' followed by C3')
- git branch -f master C3''

level 3: Juggling commits 2
- git checkout master
- git cherry-pick C2
- git commit --amend
- git cherry-pick C3

level 4: Git tags
- git tag v0 C1
- git tag v1 C2
- git checkout v1

level 5: git describe
- git commit

-------------------------------
Advanced topic:
level 1: rebasing multiple branches
- git rebase master bugFix
- git rebase bugFix side
- git rebase side another
- git branch -f master HEAD

level 2: 
- git branch bugWork HEAD~^2~

level 3: Branch Spaghetti
- git checkout one
- git cherry-pick C4 C3 C2
- git branch -f three C2
- git checkout two
- git cherry-pick C5 C4' C3' C2'
