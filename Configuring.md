## Configuring Your Pelican Site

The `pelicanconf.py` file contains all configuration variables
that [Pelican](https://github.com/getpelican/pelican) sites need to set.

Some of the configuration variables are common to all Pelican sites,
others are particular to the theme you are using.

Here's an example configuration file from 
[magic-flying-pelican](https://github.com/charlesreid1/magic-flying-pelican):

**`pelicanconf.py`:**

```python
import markdown

AUTHOR = u'charlesreid1'
SITENAME = u'ginsberg bot flock'
SITEURL = ''
PATH = 'content'
TIMEZONE = 'America/Los_Angeles'
DEFAULT_LANG = u'en'

# --------------8<---------------------
# Theme

THEME = 'gum'
# https://github.com/getpelican/pelican-themes/tree/master/gum

GITHUB_URL = ''
TWITTER_URL = ''
FACEBOOK_URL = ''
GOOGLEPLUS_URL = ''
GOOGLE_ANALYTICS_ID = ''
GOOGLE_ANALYTICS_SITENAME = ''


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

