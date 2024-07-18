# Setting up git SSH

Step 1:

```
cd ~/.ssh
ssh-keygen -o -t rsa -C "email@example.com"
cat id_rsa.pub
```

Step 2: Add key to github via SSH and GPG keys in Settings


# Git Commands

# Application

### Create empty branch

```
git switch --orphan <new branch>
git commit --allow-empty -m "Initial commit on orphan branch"
git push -u origin <new branch>
```