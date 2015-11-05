# Notes from Udacity's [How to Use Git and GitHub](1) Course

## Diffs
Keep your source code and README files to ≤ 80 columns to make diffs easier to
read.

### `diff -u`
Most systems come with either Gnu diff or a similar tool. Use this to compare
files that are not part of a git repository.

### `git diff <commit_id> <commit_id>`
The output of `git diff` is the same as `diff -u`, meaning it will have `+`
and `-` characters.

A good rule of thumb is to make one commit per logical change. For example, if
you fixed a typo, then fixed a bug in a separate part of the file, you should
use one commit for each change since they are logically separate.

## Logs
### `git log`
Show commit messages and commit IDs in reverse chronological order. This
command runs locally, not needing Internet access to the remote.

### `git log --stat`
As above, but include the number of lines added or removed.

### `git log --graph`
Display an ascii graph showing branches and merges.

### `git log --graph --oneline`
Display an ascii graph showing branches and merges, one line per commit.

## Cloning
### `git clone <url>`
Create a local copy of the repository located at the given URL.

### `git config --global color.ui auto`
Display `git` output in color. This is an alternative to [manually editing
`~/.gitconfig` to set color output](2).

git checkout <commit_id>

git diff
with no arguments. (If you don’t give git diff any arguments, it compares the
current state of your working directory to the staging area.)

git diff --staged
Compares the staging area with your most recent commit.

git rm --cached
The exact opposite of git add <filename>

git reset
If you accidentally add a file to the staging area, you can remove it using git
reset. For example, if you accidentally add lesson_2_reflections.txt, but don’t
want it to be committed yet, run git reset lesson_2_reflections.txt and the
file will be removed from the staging area, but it will still be in your
working directory.

git reset ­­--hard
Discard any changes to either the working directory or the staging area. Be
careful. This command cannot be undone. It is for removing file edits that you
never want to see again.

"commit" is a noun and a verb. As a noun it is used to refer to saved versions of files. So you commit (verb) in order to create a commit (noun).

"git init" turns a directory of files into a new repository. But you have to create the first commit yourself.

git status
Will show you which files from your working directory have been
added (via "git add") to the staging area, and which files have not been added.
This command runs locally, not needing Internet access to the remote.

git add <file>
adds a file to the staging area, but not (yet) to the repository.

git commit
Commits changes from the staging area to the repository. It also automatically opens your text editor so you can add a commit message. This is typically in the form of a command, E.g., "Add slider bar", rather than "added a slider bar".

BRANCHES:

git checkout master

git branch
With no arguments, this shows your current branches. The branch name with the
asterisk is the branch that is currently checked out.

git branch <new_name>
Creates a new named branch.

git checkout <branch_name>
Checks out a named branch. Confirm with "git branch" with no args.

git checkout -b <new_branch_name>
This is a shortcut for the following sequence of two commands:
  git branch <new_branch_name>
  git checkout <new_branch_name>
Use this when you have put yourself into "detached head mode" and you want to save your commit by creating a new branch for it. Otherwise your commit will be lost when you checkout another branch - because your commit will be "unreachable".

I--oneline <branch_1> <branch_2>
Show an ascii diagram of commit IDs and their connectivity to each other.

MERGES:

git show <commit_id>
Show a diff comparing the commit_id with its original parent commit. This is
useful after a merge has placed other commits before the commit_id you want to
learn about.

git merge <branch_name_1> <branch_name_2>
Note that you must have checked out the branch whose name you want to point
to the head commit. E.g.,

  git checkout master
  git merge master coins

Also, since the two branches are merged, the order in which they are typed into
the command line does not matter. The key is to remember that git merge always
merges all the specified branches into the currently checked out branch,
creating a new commit for that branch.

git branch -d <branch_name>
Delete a branch label, usually after a successful merge. This only deletes the
branch label, not the branch itself. The branch itself is now a parent of the
current HEAD.

git merge --abort
Restore your files to their state before you started the merge. Use this if
you get a "Merge conflict" error saying that the "Automatic merge failed". Fix
conflicts by editing the file, commit the result, then try the merge again.



REMOTES:

git remote
With no arguments, this shows the name(s) of configured remote repositories.
With the "-v" option, it shows the "fetch and "push" URLs for each configured remote repository.

git remote add <remote_name> < ssh_url | https_url >

git remote remove <remote_name>
This is useful when you have added an HTTPS URL and need to replace it with the SSH URL because you're using an SSH key and you have 2FA configured for github.com.

git push <remote_name> <branch>

git pull <remote_name> <branch>
This command is the same as running these two commands in succession:
  git fetch <remote_name>
  git merge <local_branch_name> <remote_name>/<remote_branch_name>

E.g., "git pull origin master" is the same as:
  git fetch origin
  git merge master origin/master

[1]:(https://www.udacity.com/course/how-to-use-git-and-github--ud775)
[2]:(http://unix.stackexchange.com/questions/44266/how-to-colorize-output-of-git)
