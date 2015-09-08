##### Topic 1: Introduction sequence
###### level 1: Introduction to git
<pre><code>git commit
git commit </code></pre>

###### level 2: Branching in git
<pre><code>git branch bugFix
git checkout bugFix</code></pre>

###### level 3: Merging in git
<pre><code>git checkout -b bugFix
git commit
git checkuout master
git commit
git merge bugFix</code></pre>

###### level 4: rebasing
<pre><code>git checkout -b bugFix
git commit
git checkout master
git commit
git checkout bugFix
git rebase master</code></pre>


#### Topic 2: Ramping up
###### level 1: Detach HEAD
<pre><code>git checkout C4</code></pre>

###### level 2: Relative Refs
<pre><code>git checkout C4^</code></pre>

###### level 3: Relative Refs 2
<pre><code>git checkout HEAD^
git branch -f master C6
git branch -f bugFix C0</code></pre>

###### level 4: Reversing changes in git
<pre><code>git rebase HEAD^
git checkout pushed
git revert HEAD</code></pre>


##### Topic 3: Moving work around:
###### level 1: cherry pick intro
<pre><code>git cherry-pick C3 C4 C7</code></pre>

###### level 2: Interactive rebase intro
<pre><code>git rebase -i HEAD~4</code></pre>


##### Topic 4: A mixed bag:
###### level 1: Grabbing just one commit 
<pre><code>git checkout master
git cherry-pick C4</code></pre>

###### level 2: Juggling commits
<pre><code>git rebase -i HEAD~2 (reorder the commits C3 followed by C2)
git commit --amend
git rebase -i HEAD~2 (reorder the commits C2'' followed by C3')
git branch -f master C3''</code></pre>

###### level 3: Juggling commits 2
<pre><code>git checkout master
git cherry-pick C2
git commit --amend
git cherry-pick C3</code></pre>

###### level 4: Git tags
<pre><code>git tag v0 C1
git tag v1 C2
git checkout v1</code></pre>

###### level 5: git describe
<pre><code>git commit</code></pre>


##### Topic 5: Advanced topic
###### level 1: rebasing multiple branches
<pre><code>git rebase master bugFix
git rebase bugFix side
git rebase side another
git branch -f master HEAD</code></pre>

###### level 2: Multiple parents
<pre><code>git branch bugWork HEAD~^2~</code></pre>

###### level 3: Branch Spaghetti
<pre><code>git checkout one
git cherry-pick C4 C3 C2
git branch -f three C2
git checkout two
git cherry-pick C5 C4' C3' C2'</code></pre>

![pcottle solution][pcottle_op]

###### Hooks Solution:
<pre><code>#!/bin/sh
start https://github.com/chetanpawar0989/DevOpsHW0</code></pre>

![hook solution][hook_op]

[pcottle_op]: https://github.com/chetanpawar0989/DevOpsHW0/blob/master/pcottle-git.jpg
[hook_op]: https://github.com/chetanpawar0989/DevOpsHW0/blob/master/hook.gif

