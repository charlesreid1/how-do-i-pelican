# Theming your Pelican site

Custom themes are where Pelican becomes really powerful.

For this tutorial, though, we'll stick to the basics.

See [pelican-themes](https://github.com/getpelican/pelican-themes)
on Github for a full list of themes.

See [pelicanthemes.com](http://pelicanthemes.com/)
for a gallery of themes.

## gum theme

For this example, we'll use [gum](https://github.com/getpelican/pelican-themes/tree/master/gum),
a simple Bootstrap theme.

The theme's README (linked to above) tells us what settings to include 
in our `pelicanconf.py`.

In this case, we'll leave most of these blank so they don't show up 
in the final page:

```
GITHUB_URL = ''
TWITTER_URL = ''
FACEBOOK_URL = ''
GOOGLEPLUS_URL = ''

GOOGLE_ANALYTICS_ID = ''
GOOGLE_ANALYTICS_SITENAME = ''
```

To use the gum theme, we have to install it.
Start by checking out the pelican-themes repo:

```
$ git clone --recursive https://github.com/getpelican/pelican-themes 

$ cd pelican-themes

$ pelican-themes -i gum
```

If you modify or update the theme, you can 
use the `-U` flag (for Update) with `pelican-themes`:

```
$ pelican-themes -U gum
```

Now you can set the gum theme in your `pelicanconf.py`
by setting the `THEME` variable:

```
THEME="gum"
```

