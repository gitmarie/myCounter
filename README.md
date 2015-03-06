# Counter: a simple couting app
This simple ionic app has a single button and single numeric textbox containing, initially, the number 0.
When the button is clicked, the number increases by one.
The textbox is editable, so the user can type in their own number.
The button will count from that number onwards.

## Branches
The branches just show the project in various stages.

**master:** The master branch contains the original code created by ionic from the *blank* template.

**button:** The button branch simply adds a button to index.html in the master branch. master is button's parent branch.

**number:** The number branch adds a textbox to contain the number. button is number's parent.

**model:** The model branch sets up a variable called count, which the textbox is bound to. number is model's parent branch.

**onepage:** The onepage branch just stuffs all of the app, including the logic, into index.html. It's really not recommended to do this, but is useful to understand how cordova works. model is onepage's parent.

**icon:** The icon branch doesn't have any changes to www, but it does add an icon to the app and changes it's title. It is a child of onepage.

## Exercises
These are based on the icon branch.

1. Add a reset button, that resets the count to 0.

2. Style the textbox to have the number right-justified and larger.

3. Add icons to the Count and Reset buttons.

4. Put the Reset button beside the Count button.

5. Make the reset button smaller than the Count button.

6. Persist the value of count, so that if the app is hard-restarted the previous value of count stays.

7. Separate the controller out into the file js/app.js. (This just reverses the onepage.)

## Notes

### To get your own copy of this project
You can easily get your own copy of this project in GitHub by clicking the Fork button on the project page.
This will copy all the files into your own repository of the same name (the username in front of the repository name will change to your own one.)
You can then get a copy of those files down to your own laptop of virtual machine by doing the following:

1. Look for the SSH clone URL on the GitHub page for *your* fork of the project, and click the copy button beside it.

2. At the command line, change to the directory you want to contain the app.

3. Type `git clone <url>`, where `<url>` is the URL from step 1.

From then on: you can use `git checkout <branch>` to checkout the various branches (replace `<branch>` with the branch name); you can use `git checkout -b <newbranch>` to create your own new branch (repace `<newbranch>` with the branch name);
you can send your changes up to GitHub using `git push`; and you can get new changes down from GitHub (changes made on another machine, maybe) using `git pull`.

### To update your fork
From time to time I'll change some of the code in my repository, and those changes won't automatically be applied to your fork.
Here's how to sync your fork to get my new changes.
Run these commands from your local reposity (in your virtual machine using Putty or on your own laptop at the command line).

```bash
$ git fetch upstream
$ git checkout master
$ git merge upstream/master
$ git push origin master
```

Usually all I'll change is the README.md file.

### Access denied and SSH keys
The usual way to access GitHub from the command line is by using SSH keys.
You create a unique key on the command line, tell GitHub about it, and from then on you shouldn't need your GitHub username and password each time you run a git push or pull.
If you get an error trying to clone a project, it's probably because the SSH key isn't set right.
See here on how to fix it: [GitHub Help: Generating SSH keys](https://help.github.com/articles/generating-ssh-keys/).
