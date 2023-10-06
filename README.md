# gitmergetest
A repo to play with git merges

Download repository and change directory to repository
```
git clone https://github.com/mepps/gitmergetest.git
cd gitmergetest
```


First merge
`git merge change-1`

Expected output
```
Updating 60b501b..3380a53
Fast-forward
 file | 2 ++
 1 file changed, 2 insertions(+)
```

Second merge
`git merge change-2`

Expected output
```
Auto-merging file
CONFLICT (content): Merge conflict in file
Automatic merge failed; fix conflicts and then commit the result.
```

To see which files are affected
`git status`

To see where the problem is
`git diff`

Expected output
```
++<<<<<<< HEAD
 +I love coffee
++=======
+ I love tea
++>>>>>>> change-2
```

Open file and pick the version of the code you want
HEAD is the state of the current branch
The branch name of the new branch is at the bottom

Open the file using your preferred text editor
Pick which version of the code you want
Delete all the extra characters from the merge and the code you do not want

`git commit`
