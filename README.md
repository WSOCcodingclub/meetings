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

Do the docker build step, but be warned, it takes a while to download. **Correction** See about copying from the USB flash drive to speed things up. If that doesn't work, then it might be faster to just do it on two or three machines and pair program.

Saving a docker image to an output file is `docker image save -o <save image to path> <image name>`, while loading it back again on the target computer is `docker image load -i <path to image tar file>`.

Launch the notebook, and follow along.

# February 26, 2018

First day back after ski week :snowflake: :skier: :snowflake: :snowboarder: :snowflake:

## Libraries:  os, glob, time

What are they good for?

```
os
os.getcwd()
os.chdir()
os.path.join()
os.path.split()
os.path.splittext()
os.path.real.path()
os.path.exapnduser('~')
os.stat()

time
time.localtime()

glob
glob.glob()
```

What does time look like for a computer program?

What is a globbing pattern?


## Lists, dicts, and sets

What are they, how are they used?

A unique feature to python is list comprehension (and dictionary comprehension)  (and set comprehension).

# ~March 5~ March 12, 2018

Back to Django Girls Tutorial!

With some python basics under our belt, time to get back to making a website.

## Open up the terminal

Open the terminal program, and `cd` into the `django_docker` directory (or folder, if you prefer).  Fire up the docker environment by running

```
docker-compose up
```

This creates containers for a database and for the python website.

## Create a django website---again

Earlier we created a simple django website, but we did it using the django-docker tutorial.  Now we are going to do the same thing but with the Django Girls tutorial at <https://tutorial.djangogirls.org/en/django_start_project/>.

Open up a new terminal tab or window (Command-t might work, otherwise click on the menus and look for new tab)

```
docker-compose run web bash
```

to get a bash prompt inside the docker environment.

Then open a browswer window to <https://tutorial.djangogirls.org/en/django_start_project/> and follow along:

### Make a new directory

We've already created a django project before.  Just to illustrate that this is the case, try to run

```
django-admin startproject mysite .
```

It should complain about already having a site created.

So make a new directory and re-run that command, as follows:

```
mkdir newsite
django-admin startproject mysite newsite
```

This time the command works.  What is the difference in the two lines?  One uses a dot `.`, and the other uses the full directory name `newsite`.  Take a look in newsite:

```
ls -lrta newsite
```

Now delete newsite...we don't really need it

```
rm -r newsite
```

And while we're at it, let's get rid of the old manage.py:

```
rm manage.py
```

And then finally, create the new website right here (in the `.` directory) as instructed in the django_girls tutorial

```
django-admin startproject mysite .
```


### Follow along with tutorial to edit the "mysite" django site

When you get to the part about databases, don't do what it says.  We're going to use the postgresql database, so your databases section should look like:

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}
```



## Models?

After that work is done, move on to making models at <https://tutorial.djangogirls.org/en/django_models/>

Hopefully we'll get through that as well.

(We did)

# March 19, 2018

This week the goal is to finish up the blog.  We're almost there.

## Migrations

Last week we did a lot of copy and paste, cargo-cult style
programming.  All the details on what and why we did what we did are
in the Django Girls tutorial and also in the Django documentation.
One key concept that we glossed over that should be explained a bit
more is the idea of a "migration".

When we copy and paste the code to create the "Model", we created a
blog entry with the following data items:

```
author
title
text
created_date
published_date
```

This model object is what the web server works with, but each of these
elements is just a placeholder.  The *contents* of each of these has
to be fetched from a database.  You don't just mix random authors and
titles and so on, one blog post has a specific author, title, text,
etc.  There can be many blog posts, and they all need to be saved and
retrieved when needed.

The "migrations" are instructions to the database to change its
structure in order to handle the model.  The last steps in the models
page of the tutorial that we ran last week was this:

```
python manage.py makemigrations blog
```

This *should* have created migration instructions in the file
`blog/migrations/0001_initial.py`.  If you open that file up, you will
see some stuff about dependencies and operations.  The details will be
important later, but for now all you need to know is that this file is
just a programmatically-generated program that will modify the
database to create a table called "Post" with the fields we talked
about, plus an `id` field.

Then we actually "changed" the database with

```
python manage.py migrate blog
```

## Admin

Today, we've got a little bit more spadework to do before the blog is
ready for prime time.

Follow along the tutorial at
<https://tutorial.djangogirls.org/en/django_admin/>

Then, instead of going through the next two steps related to git and
public hosting, skip ahead to
<https://tutorial.djangogirls.org/en/django_urls/>
