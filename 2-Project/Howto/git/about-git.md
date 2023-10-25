Once you have installed git, configure the information that gets logged for each of your commits by updating the default (global) credentials that git uses. (You could overwrite these credentials temporarily per local repo. While that shouldn't be necessary when working on App Academy projects, it is helpful to know that it is an option.) You will also want to set the default branch to main.

In your terminal (on Mac or WSL), run

git config --global user.name "Your Name"
git config --global user.email "Your Email"
git config --global init.defaultBranch main

Check that your name and email have been set up correctly by using the following commands:

git config user.name
git config user.email

You should see your name and email address returned. Repeat this step if there are any errors.

### Step 2
- create local repo (git init, git add, git git commit)

### Step 3
- create remote repo at github
- then
git remote add origin https://github.com/user-name/repo-name.git
git branch -M main
git push -u origin main

### step 4-9
- rest of images