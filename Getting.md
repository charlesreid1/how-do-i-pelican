# Getting Started with Pelican

There are a few things you'll need to get started with [Pelican](https://github.com/getpelican/pelican):

* (required) `pelicanconf.py` - pelican configuration file
* (required) `content/` - directory containing materials to render into a static site
* (optional) theme - either a local directory containing a theme, or a system-wide pelican theme

Use the [magic-flying-pelican](https://github.com/charlesreid1/magic-flying-pelican) 
repository as a seed repo for getting started with Pelican.

Basically, copy the contents of the `pelican/` directory
in [magic-flying-pelican](https://github.com/charlesreid1/magic-flying-pelican) 
into your own repository, and modify the contents for 
your own static site.

We'll walk through what the `pelican/` directory contains and what you 
need to change to get a simple static site up and running. 

## How Pelican Works

Let's cover the 101 of how Pelican works.

Pelican takes a pile of HTML, markdown, and other files,
and compiles them into a static site. (The advantage of
using a static site instead of a dynamic server like
Flask or a dynamic language like PHP is speed.)

To do that, it reads configuration settings from
`pelicanconf.py`, which tell Pelican where to look
for the raw files, as well as other settings like 
the theme to use.

The default location of content is the `content/`
directory, but more can be added.

The default behavior for Pelican is to serve a blog 
with a few static pages, but users can define themes
that are static pages only (no blog component).

The themes work by providing a set of static files 
and a set of HTML Jinja templates. Pelican uses
the static content and the theme to render the 
final page.

See [pelican-themes](https://github.com/getpelican/pelican-themes)
repository for themes.

See [live gallery](http://www.pelicanthemes.com/)
of pelican themes.


## Repository and Branch Layout

When using Pelican to create a static site on Github Pages,
you will need to organize your repository and set up 
branches as follows.

### Recommended way: project page

If you are hosting a project Github Pages site
(that is, a Github Pages page for any arbitrary
Github project), you should organize your repo
as follows:

* `gh-pages` branch contains all static content
* `master` branch contains the pelican site

### Uncommon way: personal page

If you are hosting a personal Github Pages site
(a repository under the account `@yourusername`
called `yourusername.github.io`), this should be 
organized as follows:

* `master` branch contains all static content
* `source` branch contains the `pelican/` directory

### Clean way: pelican as a separate branch

If you have a large project or you really don't want 
to clutter your repository branch with Pelican files,
you can also set up a three-branch model as follows:

* `master` branch contains the source code for your project (no Pelican files)
* `source` branch contains the Pelican files for your site
* `gh-pages` contains all static content for the Github Pages page


## Directory Layout

While Pelican is flexible enough to handle many
directory layouts, let's cover a common pattern:
putting markdown files into `content/`.

```
my-cool-project/

    pelican/

        pelicanconf.py

        output/
            index.html
            ...

        content/
            posts/
                blog-post-1.md
                blog-post-2.md
                blog-post-3.md
            pages/
                faq.md
                about.md
                contact.md
            img/
                my-image-1.jpg
                my-image-2.jpg
                my-image-3.jpg
```

The pelican directory contains a configuration
file `pelicanconf.py`, a folder with content
`content/`, and an output directory `output/` 
where the final static files for the site go.
(See [configuring](Configuring.md)).

The `output/` directory will not be present 
until you generate site content (see [generating](Generating.md)).

The `output/` directory should be ignored by git.
In a later section of this document we will cover
a pattern for linking output to a Github Pages
site (see [workflow: update](WorkflowUpdate.md)).

