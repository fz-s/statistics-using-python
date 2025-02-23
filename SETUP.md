# set-up instructions for Git
## 1. initial set-up based on the privacy settings
### a. Switch to SSH URL for your repository: Change the remote URL to SSH by running:
git remote set-url origin git@github.com:<user-name>/<repository-name>.git
### b. GitHub provides a special no-reply email address that you can use for commits, which will prevent your actual email address from being exposed.
git config --global user.email <git provided email from settings/emails>
### c. run SSH Agent, add key and authenticate using passphrase
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa <!-- your keyname may vary -->
ssh -T git@github.com
### d. lauch vs code from the terminal
### e. ensure that settings (json) contains this entry
"git.ssh.path": "/usr/bin/ssh"

## 2.  to create a new repository on the command line
echo "# statistics-using-python" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/fz-s/statistics-using-python.git
git push -u origin main

## 3. to push an existing repository from the command line
git remote add origin https://github.com/fz-s/statistics-using-python.git
git branch -M main
git push -u origin main
