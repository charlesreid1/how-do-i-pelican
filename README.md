# How Do I Pelican?

This is a simple explanation of how to get started
using Pelican to build a static site.
It will skip a lot of the details in the 
interest of simplicity.

The outline:

* Before you start - setting up Pelican
* Getting started with Pelican
* Configuring your Pelican site
* Setting a Pelican theme
* Generating your static site 
* Adding content to Github Pages

Workflows:

* Workflow: Initialization of the Github Pages site
* Workflow: Update the Github Pages site

## Before You Start

You'll need to have Pelican installed.
If you want to use Markdown with Pelican,
you'll also need to install Markdown.

```text
$ pip install markdown 
$ pip install pelican
```


## Getting Started with Pelican

There are a few things you'll need to get started with Pelican:

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



