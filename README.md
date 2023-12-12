# example-repo
This is the template Brian showed me

## If you need to link new github account with longleaf (should only need to do this once)
- Connect longleaf ssh keys
  - If setting up, check for existing public keys using `ls -al ~/.ssh`
  - Copy a file that looks like `id_rsa.pub` using `cat ~/.ssh/id_rsa.pub`
  - Go to profile settings on github and select the ssh key section
    - Add new key
    - Name the key appropriately
    - Paste the copied ssh key from the `cat` step above
    - Create!
- Add github credentials to longleaf
  - `git config --global user.name "your-github-username"`
  - `git config --global user.email your.email.linkedwith.github`

## Create new repo
- On github.com, create new repo
  - Add README.md and .gitignore for R
- Go to new repo, click `Code`, and copy the SSH link (should end in `.git`)
- Navigate to where you want to have the repo on LongLeaf
- Run `git clone URL-THAT-YOU-COPIED`

## Using RProj
- Open OnDemand Session
- Set working directory to new repo
- Create RProj in existing directory
- Good to go!
  - Theoretically, you can push, commit, etc. from here, but it's faster (easier?) on the terminal

## Using Git in repo
- `.gitignore` has rules to exclude files by name pattern or location
  - Don't upload data or large files!
- Changes need to be `staged` with `git add`
  - `git add .` adds all files not excluded by the `.gitignore` in the directory
  - `git add -i` opens an interactive adding session
- Commit staged changes with a note to your future self
  - `git commit -m "Hi future me, this is what I changed"`
- Commits are pushed to branches
  - For the main branch, use `git push origin main`
