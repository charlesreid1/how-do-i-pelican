# Hosting on Github Pages

Now that you've configured your [Pelican](https://github.com/getpelican/pelican) site,
created your content, viewed it, modified it,
and are happy with it, you're ready to deploy
your site somewhere viewable by the public.

Enter Github Pages.

Github provides free web hosting for static content
for _every single repository on Github_.
That means you can deploy your static site
to Github Pages for no-hassle serverless
web hosting.

(Also see the [publish](http://docs.getpelican.com/en/stable/publish.html)
page of the pelican documentation.)

## Differences between personal and project pages

In this walkthrough we assume the most common scenario
of deploying a page on Github Pages for a project.

Setting up a personal page requires changing 
branch names - see [getting started](Getting.md)
and the section on branches in particular.
Change `gh-pages` to `master` and `master` to `source`.

The rest of the document will assume you are creating
a project page.

## Where is it?

Where do Github Pages live?

If your username is `username` and your project name is `projectname`,
the Github source code is at:

```
https://github.com/username/projectname
```

and the Github Pages page will be at:

```
https://username.github.io/projectname
```


## Initializing gh-pages branch

Before you begin, you have to create a `gh-pages` branch.
We want to create a new branch that is _completely independent_
of all other branches, because this branch will only contain
the static content of our website - no code, no readmes, 
nothing but HTML, CSS, and Javascript.

We want to link the `gh-pages` branch, which will contain
the site's static content, with the `output/` directory,
where Pelican generates all of its static content.

Remove the output directory, and clone a copy of 
your repo to the output directory:

```
$ cd pelican/
$ rm -rf output/
$ git clone https://github.com/username/projectname.git output
$ cd output/
```

Now create a new orphan branch - that's the git terminology
for a branch that shares no history with any other branches.
Call it `gh-pages`:

```
$ git checkout --orphan gh-pages
```

Now all the content that was in the master branch
will show up as untracked files, because the new
`gh-pages` branch is totally empty.

Remove everything in the directory except
the `.git` directory:

```
$ rm -rf *
$ rm -rf .gitignore .gitmodules
```

Now add a simple "Hello world" page that we'll use 
to make sure our Github Pages page is being 
hosted correctly:

```
$ echo '<h2>Hello world!</h2>' > index.html
$ git add index.html
$ git commit index.html -m 'Initial commit of gh-pages branch'
$ git push origin gh-pages
```

Now we have our intiial commit on the 
`gh-pages` branch.


## Enabling Github Pages

We have one additional step to cover.
After we create the `gh-pages` branch,
we want to tell Github Pages that we have
web content on that branch that we want 
Github to host. 

Go to the repository settings,
and scroll down to the Github Pages
setting. Select the drop-down option
to host your Github Pages content
from the `gh-pages` branch.

Now visit the URL to check out your
Hello World page:

```
https://username.github.io/projectname
```

## Adding the real content

We have a hello world page working,
now let's add the real Pelican content.

Back in the `pelican/` directory,
clean out the `output/` directory
(we'll be making everything from 
scratch):

```
$ rm -rf output/*
```

Don't remove the `output/` directory itself though!

Now make the content:

```
$ pelican content
```

Now add the content to the `gh-pages` branch 
and push it to Github to deploy it:

```
$ cd output/
$ git add -A .
$ git commit -a -m 'Updating site'
$ git push origin gh-pages
```

This will push the new static site (this time with 
the Pelican output) to the `gh-pages` branch on Github.
Sometimes the site updates really fast (few seconds),
sometimes it takes longer, but never more than about a minute.

Don't forget to add a link to your new page
in the repository description (and in your README)
to make it easier to find!

