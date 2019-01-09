GitHub: How not to lose your entire analysis!
===

## What is Git and why use it?

Version control is essential in creating any project that  takes longer than 5 minutes to complete. Even if your memory is longer than 5 minutes, next month you are not likely to be able to retrace your steps.

Version control will allow you to back up every point at which you analysis is standing, provided you actively identify those points yourself. Imagine that every time you press the save key on a word document, every change between the last time you saveed and now was saved in a different version of the document. This way, you're only viewing the final version of your text, but if you wanted to, you could go back and view all of the old versions.

![](https://i.imgur.com/Foktz0Z.gif)

When you are doing this yourself, this can get cumbersome, so let git do it for you!

## Options in Git

The name of the software you're running is __git__, and you can use commands in a similar fashion as what you've learning in __bash__. The syntax here is:

```
git verb options
```

In git, there are different git commands (verbs) and different options for those commands.

### Configuring global options

When you start using git, you build repositories, which hold all the scripts and notes for each of your projects. It is recommended that you use one repository for each project.

In order for git to recognize you as the owner of those repositories, you need to first set up the global options for git on your virtual (or personal) machine.

```
$ git config --global user.name "Elias Oziolor"
$ git config --global user.email "emoziolor@ucdavis.edu"
```

I told git who I am and where to find me. Make sure that this is the same e-mail address that you have or will open a __GitHub__ account with.

### Initiating a repository

Once you've chosen a location for all of your work on this project, in our case the __~/project__ directory, you can create a repository for this project.

```
cd ~/
mkdir project
```

__What is a repository__: A repository is the location, in which a set of files will be backed up. Use a single repository for each project.

__Sample setup__: I like to include two folders in my repositories: 1) data; 2) scripts.

To start a repository type the following in the folder which contains all other folders:

```
git init
```

If you type the command ```ls -a```, you will be able to see that there is a .git file in the folder, which is not your git repository.

### Handling a repository

Once you have a repository, let's start using it to back things up. There are several terms that you need to be familiar with to be comfortable with git:

__Staging files__: When you __stage__ files for commit, this means that you are telling git to save the changes in these particular files in the commit that you are about to do.

__Commit__: When you perform a commit, you log any changes to staged files and lock those changes to this particular time.

__Commit message__: When you perform a commit, you are allowed to enter a message, which will later be used to remind you what you did in this particular chunk of work that you commited. __IMPORTANT__: Make sure those messages are informative! 3 months from now, you might want to get back to something that is no longer working and figure out where the issue originated, if you make generic commits messages like "Worked on file.txt", you'll be in deep trouble.

### Staging

Now that you've started a repository (or a repo), let's create some folders:

```
mkdir data
mkdir scripts
```

Now, in most cases, the data you have in your data folder will be way too large to commit in git. Git is created to commit code and small amounts of text. What we need to do is __ignore__ everything that is too large.

We do this by creating a ```.gitignore``` file, which contains all of the directories or types of files that we would like to ignore. It starts with a __.__ because it is a "hidden" file. Meaning if we type ```ls```, we won't be able to see it. We would need to specify ```ls -a```

```
touch .gitignore
nano .gitignore

/data
*.fasta
```

Now we've created a file, which will force git to ignore everything that is in the folder ```/data``` and any file that is of the filetype ```fasta```. You can do this with any folder or filetype you would like!

Let's start with our first __commit__. We want to first stage the ```.gitignore``` file.

```
git add .gitignore
git status
```

Now the message that git shows you should be that your .gitignore file is in green (staged for commit), while eall other files/folders are in red (not staged).

We can start by committing this set of changes:

```
git commit -m "Initial commit: .gitignore file for /data and fasta"
```

There we go! First commit is done. To track what happened you can type:

```
git log
```

in the repository folder and that will show you a set of commits that you've done so far.

While you now have your first commit, you can start committing everything else in your repo without worries that it is too large (because now git will ignore tha large things).

```
git add --all
```

This command will stage every change you've made since your last commit.

```
git commit -m "Commit of initial repository setup"
git log
```

If you are wondering if all the files are truly staged for commit before you commit them, you can check again with ```git status```

### Backing up your repositories with GitHub

Great! Now you have a repo with 2 commits. This is locally backed up now, but what if you lose your computer? This is another strong asset of git - it can back up files remotely.

Let's go to GitHub.com and create a profile. If you have one already, take a second to admire your work.

Once you have set up a profile, it's time to create a repository in github, which will then receive all the backups from the repository you created on your machine.

Go to your profile and add click the __plus__ button.

<img src="https://i.imgur.com/wGFfeSd.png" width="1200" height="800">

Then fill out the necessary information for your repository to be distinct and recognizeable.

![](https://i.imgur.com/MJszSW8.png width="1200" height="800")

When you've created the repository, GitHub will tell you what you need to do in order to sync your two repositories into one.

Only use the last two lines, because you've already committed changes!

![](https://i.imgur.com/HZNr7XL.png =1200x800)

Once you execute those two lines in your terminal, you should be able to see a reflection of your local repository online.

Every time you type:

```
git push origin master
```

You will force git to back up all of your commits since the last time you __pushed__ to be backed up online. FOR FREE!

## Suggestions for good Git Usage:

1) commit in recognizeable chunks of work
2) commit more often than you think you should!
3) place informative messages with every commit
4) code a bunch!
