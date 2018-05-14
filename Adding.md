# Adding content to your site

Now that you have generated your site with the 
`pelican` command, and have used Python to serve
your documentation with a simple HTTP server,
you have all the tools you need to start creating
content for your website.

Also see [writing content](http://docs.getpelican.com/en/stable/content.html)
page of pelican documentation.

Pelican has two types of content: pages (unchanging, no chronology) 
and articles (blog posts). We will cover each below.

## Adding blog posts to your site

Let's cover how you add new content to your site.

By default, Pelican is set up to create blog sites,
so we'll cover how to create a blog. Creating static
sites requires custom themes, and we won't get into that
in this document.

In the `content/` directory (or `content/posts/` directory), 
you create blog posts by adding Markdown files, and specify
metadata using a YAML header.

Here's a Markdown template for a blog post:

```
Title: My super title
Date: 2010-12-03 10:20
Modified: 2010-12-05 19:30
Category: Python
Tags: pelican, publishing
Slug: my-super-post
Authors: Alexis Metaireau, Conan Doyle
Summary: Short version for index and feeds

This is the content of my super blog post.
```

Note that not everything is necessary (e.g., Slug, Authors, Summary).
Ultimately the variables in the YAML headers of each
blog post are passed to the theme's page templates,
so what information gets used depends on the theme 
that you use.

## Adding pages to your site

Metadata for 

## Linking to other pages

As shown in the [linking to internal content](http://docs.getpelican.com/en/stable/content.html#linking-to-internal-content)
section of the pelican docs, you can link to other files

**`article1.md`:**

```plain
Title: The first article
Date: 2012-12-01 10:02

See below intra-site link examples in Markdown format.

[a link to another file]({filename}/article2.md)
```

**`article2.md`:**

```plain
Title: The second article
Date: 2012-12-01 10:02

More markdown goes _here_.

[link back to article one]({filename}/article1.md)
```

See [docs](http://docs.getpelican.com/en/stable/content.html#linking-to-internal-content) for details.


## Linking to static files

For example, a project’s content directory might be structured like this:

Suppose you have a directory structure like this:

```
content
├── images
│   └── han.jpg
├── pdfs
│   └── menu.pdf
└── pages
    └── test.md
```

then in `test.md` you would link to other files like this:

```
![Alt Text]({filename}/images/han.jpg)
[Our Menu]({filename}/pdfs/menu.pdf)
```

See [docs](http://docs.getpelican.com/en/stable/content.html#linking-to-internal-content)
for details...

