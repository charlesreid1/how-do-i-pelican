# Theming your Pelican site

Custom themes are where Pelican becomes really powerful.

For this tutorial, though, we'll stick to the basics.

See [pelican-themes](https://github.com/getpelican/pelican-themes)
on Github for a full list of themes.

See [pelicanthemes.com](http://pelicanthemes.com/)
for a gallery of themes.

## simple-bootstrap theme

For this example, we'll use the [simple-bootstrap](https://github.com/getpelican/pelican-themes/tree/master/simple-bootstrap),
a simple Bootstrap theme.

To use the simple-bootstrap theme, we have to install it.
Start by checking out the pelican-themes repo:

```
$ git clone --recursive https://github.com/getpelican/pelican-themes 

$ cd pelican-themes

$ pelican-themes -i simple-bootstrap
```

If you modify or update the theme, you can 
use the `-U` flag (for Update) with `pelican-themes`:

```
$ pelican-themes -U simple-bootstrap
```

Now you can set the gum theme in your `pelicanconf.py`
by setting the `THEME` variable:

```
THEME="simple-bootstrap"
```

