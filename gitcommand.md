# Git Commands

### Change branch

```
git checkout [name_branch]
```



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

