# Answers to questions posed in Lesson 1 of Udacity's [How to Use Git and Github][1] course.

*How did viewing a diff between two versions of a file help you see the bug
that was introduced?*

>It made it easy to visually spot the character that had changed because it was
lined up with the unchanged string on the next line.

*How could having easy access to the entire history of a file make you a more
efficient programmer in the long term?*

>It could help you remember the sequence of your thinking process as you made
changes to your code. It could also help you figure out where you made a
mistake that caused a cascading problem.

*What do you think are the pros and cons of manually choosing when to create a
commit, like you do in Git, vs having versions automatically saved, like Google
docs does?*

>__Pros:__ Manually choosing when to commit allows the version history to
become a record of the major events in the programmer's thinking process while
he/she was creating the code. Also, it allows the version history to not be
cluttered with arbitrary versions of the code which, incidentally, may or may
not even compile.

>__Cons:__ The major weakness of allowing the programmer to manually choose
when to commit is that he/she may be undisciplined or inconsistent in choosing
when or even if, to commit.

*Why do you think some version control systems, like Git, allow saving multiple
files in one commit, while others, like Google Docs, treat each file
separately?*

>Version control systems for interrelated files, such as source code, need to
be able to track multi-file changes together as a single change. But document
revision control systems don't need to support (as many) relationships between
individual files.

*How can you use the commands `git log` and `git diff` to view the history of
files?*

>The `git log` command shows the unique 40 digit *commit id* of each change,
who made each commit, when they did it, and the comment they added. With the
`--stat` option you can also see the number of lines they removed and added
from each file.

>The `git diff` command shows the lines which have changed, and what they
looked like before.

*How might using version control make you more confident to make changes that
could break something?*

>I will always know that I have an easy way to revert back to code that I know
works.

*Now that you have your workspace set up, what do you want to try using Git
for?*

>I want to build a portfolio of projects. But at first I may try using it to
fix the asteroids code bug. I'm hoping that that is what this course will show
in the next lesson.

[1]: https://www.udacity.com/course/how-to-use-git-and-github--ud775
