# Local branching, merge to main, but in the mean time, origin main was updated

```bash
git checkout -b Phil
git add.
git commit -m"first commit"
git add.
git commit -m"second commit"


```

On origin main

```bash
git checkout main
git add.
git commit -m"first commit from origin main"
git add .
git commit -m"second commit from origin main"


```

Back on main

```bash
git checkout main
# alert, tip of branch is 2 commits behind, pull before...

git merge master
# error

```

Solved by 

```bash
git checkout main
git fetch
git merge
# solve conflict
git merge Phil

```