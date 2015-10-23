# Answers to questions posed in Lesson 3 of Udacity's [How to Use Git and Github][1] course.

*When would you want to use a remote repository rather than keeping all your
work local?*

>When collaborating with another developer; when developing from more than one
computer; when you want others to be able to access and edit your code.

*Why might you want to always pull changes manually rather than having Git
automatically stay up-to-date with your remote repository?*

>You want to have strict control over the code base you're working on. Choosing
to temporarily be out-of-sync might be exactly what you want to do while you're
taking the code in a new direction. Automatic pulls could disrupt this
scenario.

*Describe the differences between forks, clones, and branches. When would you
use one instead of another?*

>A *fork* is a clone of a repository you don't own, which has been cloned from
a remote repository to your remote repository. Note that both repositories are
on github, but you only own the latter. Forking another person's repository via
the fork button on github.com allows that person to get credit for having
been the original owner of the code before you forked it. Forking is also a
convenient shortcut for cloning another person's repository to your repository.
The fork shortcut eliminates the need to clone to your local machine and push
to your own remote repository. Use fork, rather than clone, when you plan to
make modifications to code you got from somebody else's repository.

>A *clone* is a copy of a remote repository which you've copied (cloned) to
your local machine. The remote repository may or may not be owned by you. For
repositories you don't own, use clone, rather than fork, when you simply
need to possess a copy of their files, such as when all you intend to do is to
compile and/or install their code on your local machine. For repositories you
do own, use clone to allow your local machine, i.e., a second PC or laptop, to
create, modify, and push changes to files hosted on the remote repository.

>Another use case for *clone* over fork is when you are a contributor to a code
base owned by somebody else. In this case you would clone the remote repository
(which you don't own), make your modifications locally on your machine, then
push the changes to their remote repository, if they have given you permission
to do so. If they have not given you that permission, I assume that is where
pull requests come in. But that is probably in the next video.

>*Branches* are used to take your code in a new direction, via a mnemonic
label, without disrupting the existing code's stability. If you already have
the code in your local repository you would not clone it, and forking does not
apply in this case either. In this case you would create a new branch which
would point to a specific commit which contains modifications to your code that
are experimental, substantially disruptive, or introduce a significant new
feature which is not yet stable enough for the master branch of your code.

*What is the benefit of having a copy of the last known state of the remote
stored locally?*

>The primary benefit of having a local copy of the last known state of the
remote is that it allows git to know if you are ahead, behind, or out-of-sync
with the remote repository. A secondary benefit is that you can manually view
the log or diffs of the remote before you merge your branch (e.g., master) with
the code from the remote (e.g., origin/master).

[1]: https://www.udacity.com/course/how-to-use-git-and-github--ud775
