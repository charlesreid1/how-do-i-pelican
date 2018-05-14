# Serving your static site

Once you've run the `pelican` command to generate
your static site, you'll want to see what it looks like.
To do this, you need to run a simple HTTP server - 
nothing fancy. 

(Now you can see the advantage of a static site.)

Run a simple HTTP server with python, which has a 
built-in HTTP server that can be run from the 
command line.

Run the server from the `output/` directory,
which contains the static content for your site.

```
$ cd pelican/output/

$ python -m http.server    # serve content on localhost:8000

$ python -m http.server 8888  # serve content on localhost:8888
```

Now navigate to `localhost:8000` or `localhost:8888` 
in your browser to view your static site.

