<!-- INSTRUCTIONS GO HERE -->
#  create a new repository on the command line
echo "# statistics-using-python" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/fz-s/statistics-using-python.git
git push -u origin main

# push an existing repository from the command line
git remote add origin https://github.com/fz-s/statistics-using-python.git
git branch -M main
git push -u origin main

# Switch to SSH URL for your repository: Change the remote URL to SSH by running:
git remote set-url origin git@github.com:<user-name>/<repository-name>.git
