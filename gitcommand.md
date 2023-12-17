# Setting up git SSH

Step 1:

```
cd ~/.ssh
ssh-keygen -o -t rsa -C "email@example.com"
cat id_rsa.pub
```

Step 2: Add key to github via SSH and GPG keys in Settings


# Git Commands

### Change branch

```
git checkout [name_branch]
```
Thêm '-b' là tạo mới branch và chuyển sang branch mới



# Application

### Rollback last push
```
git reset --hard <revision_id_of_last_known_good_commit>
git push --force
```
Example:
```
git reset --hard HEAD^
git push --force
```

Note: use when nobody pull last push

### Create empty branch

```
git switch --orphan <new branch>
git commit --allow-empty -m "Initial commit on orphan branch"
git push -u origin <new branch>
```

### Tạo một nhánh mới và push code sau đó tạo pr

git checkout -b <new branch>

-> Cherry-pick branch main

git push --set-upstream origin <new branch>


### Gom các commit

```
git reset --soft HEAD~<number_of_commit>
git add .
git commit --amend -m <commit_name>
git push -f 
```

### Merge với nhánh sota-testing

```
git checkout -b refactor/get-token-metadata-sota-testing
git fetch
git merge origin/sota-testing
git add .
git status
git commit -m "chore: merge sota-testing"
git push -u origin refactor/get-token-metadata-sota-testing
```