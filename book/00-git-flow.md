## Git flow

### 1. Work on new brand

Check out from master or dev branch: `git checkout -b your-new-branch`

### 2. After finished your work. Add your change to staged and commit it

`git add .` or `git add your-file-name`

`git commit -m "Commit's message"`

### 3. After commit, merge the latest code from remote branch

#### 3.1. The first way - Use MERGE

- Pull the latest code: `git pull origin dev` or `git pull origin master`
- Fix the conflict if you have and commit it

#### 3.2. The second way - Use REBASE

- Checkout to master (or dev): `git checkout master`
- Pull the latest code: `git pull origin master`
- Checkout back to your new branch: `git checkout your-new-branch`
- Rebase master: `git rebase master`
- Fix the conflict if you have and then add it to staged `git add .`
- After that, use `git rebase --continue`

### 4. Push your branch

`git push origin your-new-branch`

### 5. Create Merge Request on remote repository
