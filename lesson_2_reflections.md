# Answers to questions posed in Lesson 2 of Udacity's [How to Use Git and Github][1] course.

*What happens when you initialize a repository? Why do you need to do it?*

> Git creates a `.git` directory in your current working directory. But you still don't have any commits, so `git log` won't have any entries.

*How is the staging area different from the working directory and the
repository? What value do you think it offers?*

 >The staging area is different from the working directory in that the working
directory can contain files that are not (yet) in the staging area. The staging area is different from the repository in that files in the staging area have not yet been committed into the repository. Because of this, changes to files in the staging area will not show up in the output of `git log`.

*How can you use the staging area to make sure you have one commit per logical change?*

>Right before you run `git commit` you can run the following commands to make sure that you only have one change in the staging area:

    git diff (with no arguments)
    git diff --staged
    git status

*What are some situations when branches would be helpful in keeping your
history organized? How would branches help?*

>Experimental new features; refactored code that has not yet been tested;
special case versions of your code, such as for running in legacy environments.

*How do the diagrams help you visualize the branch structure?*

>They can help you get oriented in reference to a specific commit that you remember or that you want to use. They can also help you understand why certain commits are not included in the output of `git log` for certain branches - those commits may have happened after the new branch split off from the master branch or from whatever branch you have currently checked out.

*What is the result of merging two branches together? Why do we represent it in the diagram the way we do?*

>The resulting merge is a union of the lines of code from both branches, minus any common lines that were deleted in one or both branches. This means that lines added in either of the branches are added to the merged branch. The diagram was represented the way it was so that we could clearly see the reachability of each branch's parent commits, or the lack there of.


*What are the pros and cons of Git’s automatic merging vs. always doing merges manually?*

>At this point, without more actual experience, I can't really say what the pros are beyond the obvious labor savings. I'd say the same for the cons. It really depends on how often the automated merges produce unexpected outcomes.

[1]: https://www.udacity.com/course/how-to-use-git-and-github--ud775
