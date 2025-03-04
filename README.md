Sampa group website
===================

This is the [Sampa group website](http://sampa.cs.washington.edu), built with [Jekyll][] and [bibble][].

It's based on our [research group website template](https://github.com/uwsampa/research-group-web), which you can use to build your own nice group website! 🎣

Gitpod for incredibly easy building and deploying
-------
With gitpod you can easily create a website.

* Fork this repository
* Change Open in Gitpod button on README.md file.
* Click and open gitpod.
* Change content (when Jekyll serving docs files will be automatically generated)
* Commit changes and push into a repository
* Configure Github pages and select docs folder for static page destination
* Congratulations.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/your-github-username/your-repository)

Editing
-------

Most pages are just Markdown files that you can edit directly. People are
listed in `_data/people.yml` and the news is generated from Markdown files in the `_posts` folder.

Try editing directly in GitHub! It's like magic.


News Items and Blog Posts
-------------------------

For both long-form blog posts and short news updates, we use Jekyll's blogging system. To post a new item of either type, you create a file in the [_posts directory][postsdir] using the naming convention `YYYY-MM-DD-title-for-url.md`. The date part of the filename always matters; the title part is currently only used for full blog posts (but is still required for news updates).

The file must begin with [YAML front matter][yfm]. For news updates, use this:

    ---
    layout: post
    shortnews: true
    ---

For full blog posts, use this format:

    ---
    layout: post
    title:  "Some Great Title Here"
    ---

And concoct a page title for your post. The body of the post goes after the `---` in either case.

[yfm]: http://jekyllrb.com/docs/frontmatter/
[postsdir]: https://github.com/uwsampa/sampa-www/tree/master/_posts


Building and Deploying
----------------------

The requirements for building the site are:

* [Jekyll][]: run `gem install jekyll`
* [Pybtex][]: run `pip3 install pybtex`
* [bibble][]: run `pip3 install bibble`
* ssh and rsync, only if you want to deploy directly.

`make` compiles the bibliography and the website content to the `_site`
directory. To preview the site, run `jekyll serve`` and head to
http://0.0.0.0:4000.

To upload a new version of the site via rsync over ssh, type `make deploy`. ~A web hook does this automatically when you push to GitHub.~

If you use an alternative Python when building the bibliography, use `make
PYTHON=/path/to/python`.

[Jekyll]: http://jekyllrb.com/
[bibble]: https://github.com/sampsyo/bibble/
[pybtex]: http://pybtex.sourceforge.net

TODOs, Known Issues
----------------------
+ Lab hooknook is not working
+ Polish up frontpage, re-integrate projects for the new decade
