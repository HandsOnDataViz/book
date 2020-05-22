# My GitBook Workflow
*By [Jack Dougherty](../../introduction/who.md), last updated December 8, 2016*

GitBook offers different ways to compose your books, and each method has its own advantages. Typically, I compose text using the GitBook web editor or desktop editor, or modify files with the Atom text editor and push these changes to my GitHub repository with GitHub Desktop. None of these steps require using Git on the command line.

## Compose with GitBook WEB Editor:

Advantages: WYSIWYG preview, Markdown menu, proofreader toggle, branch control

1. Check GitHub repo for any pull requests from contributors: https://github.com/JackDougherty/
2. Startup browser editor, temporarily create a new branch (dev) to avoid continually building master branch
3. Write and save edits on each page
4. When done, merge branches (push dev branch into master branch)
5. When done, delete the dev branch to avoid confusion in future

## Compose with GitBook DESKTOP Editor

Advantages: WYSIWYG preview, Markdown menu, proofreader toggle, branch and sync control

Disadvantage: links and images appear, but requires clicking on Markdown version to edit

1. Check GitHub repo for any pull requests from contributors: https://github.com/JackDougherty/
2. Startup Desktop Editor app and CLONE current book from GitHub to local computer
3. Create a temporary new branch (dev)
4. Write and save edits on each page
5. When done, merge branches (push dev into master) and sync
6. Delete the dev branch to avoid confusion
7. Delete the CLONE of the book from my local computer to avoid confusion

## Compose with Atom Editor and GitHub Desktop

Advantages: This method works best when making major changes to the book, such as reorganizing the folder-file structure, rethinking the table of contents, and adding images into specific folders.

Disadvantages: For novice users, requires basic knowledge of GitHub web interface, GitHub Desktop, and a text editor (such as Atom Editor)

1. Check GitHub repo for any pull requests from contributors: https://github.com/JackDougherty/
3. Use GitHub Desktop to sync repo to my local computer
4. Use Atom editor to edit, upload, restructure files
5. Use GitHub Desktop to commit changes to online repo master branch

## My Settings
- TO DO: explain GitBook-GitHub link; custom domain



{% footer %}
{% endfooter %}
