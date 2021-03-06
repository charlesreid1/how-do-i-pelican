## Configuring Your Pelican Site

The `pelicanconf.py` file contains all configuration variables
that [Pelican](https://github.com/getpelican/pelican) sites need to set.

Some of the configuration variables are common to all Pelican sites,
others are particular to the theme you are using.

Here's an example configuration file from 
[magic-flying-pelican](https://github.com/charlesreid1/magic-flying-pelican):

**`pelicanconf.py`:**

```python
AUTHOR = 'charlesreid1'
SITENAME = 'how-do-i-pelican'
SITEURL = ''
PATH = 'content'
TIMEZONE = 'America/Los_Angeles'
DEFAULT_LANG = 'en'

# --------------8<---------------------
# Theme

THEME = 'simple-bootstrap'
# https://github.com/getpelican/pelican-themes/tree/master/simple-bootstrap


# --------------8<---------------------
# Files and content


# This will look for a directory img/ 
# inside the directory content/
# The contents of img/ will be available at 
# {{ SITEURL }}/img
STATIC_PATHS = ['img']

# If we want to create static pages,
# we should put them in content/pages
PAGE_PATHS = ['pages']

# If we want to create blog posts (articles),
# we should put them in content/posts
ARTICLE_PATHS = ['posts']


# --------------8<---------------------
# idk just some dumb stuff

DISPLAY_PAGES_ON_MENU = False
FEED_ALL_ATOM = None
CATEGORY_FEED_ATOM = None
TRANSLATION_FEED_ATOM = None
AUTHOR_FEED_ATOM = None
AUTHOR_FEED_RSS = None
DEFAULT_PAGINATION = False
```

This will configure the `content/` directory
to contain a `posts/` folder with blog posts
and a `pages/` folder with static pages.

There's a lot more that can be done with the 
configuration file, but much of it requires
custom themes, so we'll leave it at that.

See the [settings page](http://docs.getpelican.com/en/stable/settings.html?highlight=configuration)
of the pelican documentation for details.

