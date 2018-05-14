# Generating your static site

To generate your static site with [Pelican](https://github.com/getpelican/pelican),
use the `pelican content` command, run from
the `pelican/` directory (see [getting started](Getting.md)
for a guide to the pelican directory layout):

```plain
$ pelican
```

This will generate the static site content into
the `output/` folder.

Inputs: `content/`

Output: `output/`

To modify the input folder, change the `PATH` variable
in `pelicanconf.py`:

```plain
PATH = 'my_custom_content_dir'
```

To modify the output directory, set the 
`OUTPUT_PATH` variable in `pelicanconf.py`:

```plain
OUTPUT_PATH = 'my_custom_output_dir'
```

See the [settings page](http://docs.getpelican.com/en/stable/settings.html)
of the pelican documentation for more variables
that can be set in the `pelicanconf.py` file.

