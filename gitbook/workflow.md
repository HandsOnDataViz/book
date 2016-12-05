# My GitBook Workflow

## My Settings
- TO DO: explain GitBook-GitHub link; custom domain

## Write with GitBook BROWSER Editor:

Advantages: WYSIWYG preview, Markdown menu, proofreader toggle, branch control

1. Check GitHub repo for any pull requests from contributors: https://github.com/JackDougherty/datavizforall
2. Startup browser editor, create a new branch (dev) to avoid continually building master branch
3. Write and save edits on each page
4. When done, merge branches (push dev branch into master branch)
5. When done, delete the dev branch to avoid confusion

## Write with GitBook DESKTOP Editor

Advantages: WYSIWYG preview, Markdown menu, proofreader toggle, branch and sync control

Mixed opinion: links and images appear, but requires clicking on Markdown version to edit

1. Check GitHub repo for any pull requests from contributors: https://github.com/JackDougherty/datavizforall
2. Startup Desktop Editor app and CLONE current book from GitHub to local computer
3. Create a new branch (dev)
4. Write and save edits on each page
5. When done, merge branches (push dev into master) and sync
6. Delete the dev branch to avoid confusion
7. Delete the CLONE of the book from my local computer to avoid confusion


## Structural changes with GitHub Desktop and Atom Editor
When making major changes to the book, especially folder/file structure, copy a branch to a local computer with GitHub Desktop, and modify with Atom Editor (or your preferred text editor).
1. Check GitHub repo for any pull requests from contributors: https://github.com/JackDougherty/datavizforall
2. Create dev branch for current edits
3. Use GitHub Desktop to sync repo to my local computer, where dev branch is default view
4. Use Atom editor to edit/upload/restructure files
5. Use GitHub Desktop to commit changes to online repo dev branch, send pull request to master branch, and confirm it online
6. Delete the dev branch from GitHub repo to avoid confusion


{% footer %}
{% endfooter %}
