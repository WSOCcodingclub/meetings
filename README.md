# meetings
Track weekly meetings

This should be used to track club meetings.  For now just add notes here.  Later maybe break things up into one document per meeting.

# 2018

## Jan 8 Meeting

First day back after Christmas Break.  The meeting is on for those who can make it.

### Code Editors

* Emacs via [spacemacs](https://github.com/syl20bnr/spacemacs/tree/develop/layers/%2Bdistributions/spacemacs-docker)

* Vi via vim

* Microsoft [visual studio code](https://code.visualstudio.com/Download).  Alternate Docker setup [here](https://hub.docker.com/r/jess/vscode/) but that's to complicated.

### What's a for loop for?

Go over a for loop.  Try to sort something. [Tutorial link](https://tutorial.djangogirls.org/en/python_introduction/#loops).  Python [docs link](https://docs.python.org/3/reference/compound_stmts.html#the-for-statement)

## Jan 22 Meeting

First day back after yet another break!

* Make sure laptops all have VSCode (see link above)
* Make sure laptops are all running Docker, etc etc, and have the sample project loaded (https://github.com/WSOCcodingclub/django_docker)
* load up the simple for loop program from last time ([Tutorial link](https://tutorial.djangogirls.org/en/python_introduction/#loops)).

### Sorting a list

Today we're going to sort that list of names that we displayed in the old program.  This will teach lots of small but important aspects of programming, including `if` statements, temporary variables, looping, and so on.

1. copy the file `Python_intro.py` to a new file called `sorting_list.py`
2. open up `sorting_list.py` in the VSCode editor
3. collaborate on sorting that list of names (alphabetically):
    girls = ['Rachel', 'Monica', 'Phoebe', 'Ola', 'You']
    
Think about how you would alphabetically sort that list in your head.  Try to write down exactly what your brain is doing.  That is an algorithm.  We'll turn that algorithm into code, and then see how well it does.

## Jan 29 2018

Last time was just Catherine, so maybe we should repeat!

Go get Catherine's progress from last time, as follows:

1. change into the folder with django_docker on your computer.  Probably just doing `cd django_docker` will work.
2. add Catherine's repository as a new source:
```
git remote add seagulsong https://github.com/seagulsong/Docker-Python
```
3. "fetch" Catherine's changes:
```
git fetch seagulsong
```
4. create a new branch in git for today's work.  
```
git checkout -b sort_array
```
The "checkout" command will switch to an existing branch, and the "-b" flag tells git to make a new branch if it doesn't already exist.
5. merge Catherine's latest change with your code by "cherry-picking" her most recent commit.  First inspect Catherine's logs to find the right commit number. Then run the cherry-pick command to apply just that commit to your code.
```
git log seagulsong/master
```

(Copy the commit number that you see in the log.  It will look like a long string of letters and numbers, like "ac925feeef8a...")

```
git cherry-pick [that long string of letters and numbers]
```

The output should be:

```
 sorting program
 Author: WSOCHS Student <wsochsstudent@WSOCHS4s-MacBook-Pro.local>
 Date: Mon Jan 22 16:11:46 2018 -0800
 1 file changed, 16 insertions(+)
 create mode 100644 sortinglist.py
```

### Meeting notes

#### New laptops

Pia noted that 20 through 25 have Docker, git, and visual studio code installed.

#### UNIX commands

We used `cd`, `ls`, `ls -lrt`, `ls -lrta`, `ls -lR .git`

#### git commands

We used `git commit -a`, `git status`, `git checkout sortinglist.py` to erase our work, 
`git remote add <name> <url>`, `git fetch`, `git cherry-pick`, and maybe some others.

#### python code

We used a for loop, and if statement, and comparison of strings using < (less than).  
We also wrote an infinite loop by having the hi() function call itself (recursion).

#### ToDo items

- [ ] bug the club members who haven't been coming to come.  
- [ ] ask Lauren to add Emma K (username?), maybe others, to the WSOCcodingclub group

# February 5, 2018

Jupyter notebooks today...maybe

Clone this repository: https://github.com/jmarca/jupyter_notebook_intro

```
git clone https://github.com/jmarca/jupyter_notebook_intro
```

Then switch into the newly created directory called "jupyter_notebook_intro" and read the README.

Do the docker build step, but be warned, it takes a while to download.  Maybe just do it on two or three machines and pair program.

Launch the notebook, and follow along.
