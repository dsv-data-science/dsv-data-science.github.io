
# Research Group website template

**Credits**

This project is based on the [repository](orig_repo) provided by the University of Washington. The website of the original creators can be accessed [here][sampa].

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License][license].

[orig_repo]: https://github.com/uwsampa/research-group-web
[sampa]: http://sampa.cs.washington.edu/
[license]: https://creativecommons.org/licenses/by-nc/4.0/

**Changes**

The original template was modified as follows:
- Enable `.bib`  compilation from Jekyll using [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar) instead of requiring python package bibble.
- A deploy file was generated to upload it to GitHub pages, even though some jekyll-scholar is not compatible with GitHub. The deploy file is based on [another Jekyll template](https://github.com/alshedivat/al-folio/blob/master/bin/deploy)


## Features

* Thanks to [Jekyll][], content is just text files. So even faculty should be able to figure it out.
* Publications list generated from BibTeX.
* Personnel list. Organize your professors, students, staff, and alumni.
* Combined news stream and blog posts.
* Easily extensible navigation bar.
* Responsive (mobile-ready) design based on [Bootstrap][].

[Bootstrap]: http://getbootstrap.com/


## Setup

1. Install the dependencies. You will need [Ruby][], then install Jekyll and bundler
   -  ` gem install jekyll bundler`
2. [Fork][] this repository on GitHub.
3. Clone the fork to your own machine: 
   - `git clone git@github.com:yourgroup/research-group-web.git`
4. Check that you use the `source` branch of the repo while development purposes. `master` is used for deployment of the static website and avoid CI/CD in GitHub (which does not support compilation of `.bib`).
5. Customize. Start with the `_config.yml` file, where you enter the name of the site and its URL.
6. Keep adding content. See below for instructions for each of the various sections.
7. To start your local server
   - `bundle exec jekyll serve`
8. To deploy your website to GitHub pages in the `master` branch
   - `./bin/deploy --user`
9. Finally, your website should be allocated in the folder `_src` and automatically committed to the repository.

[Ruby]: https://www.ruby-lang.org/en/
[Fork]: https://github.com/uwsampa/research-group-web/fork



## Publication List

The list of publications is in `bib/papers.bib`. These are compiled and grouped per year. Each co-author that is part of the group (edit in `_data/people.yml`) will have a link that point to their website (if specified).

## News Items and Blog Posts

For both long-form blog posts and short news updates, we use Jekyll's blogging system. To post a new item of either type, you create a file in the `_posts` directory using the naming convention `YYYY-MM-DD-title-for-url.md`. The date part of the filename always matters; the title part is currently only used for full blog posts (but is still required for news updates).

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

You can also customize the icon that is displayed on the news feed. By default it's `newspaper-o`. We use icons from the [FontAwesome][fa] icon set.

[yfm]: http://jekyllrb.com/docs/frontmatter/
[fa]: http://fontawesome.io/icons/

## Projects

To create a project, just create a markdown file in the `_projects` folder. Here are the things you can put in the YAML frontmatter:

- `title:` The project title.
- `notitle:` Set this to `true` if you don't want a title displayed on the project card. Optional.
- `description:` The text shown in the project card. It supports markdown.
- `people:` The people working on the project. This is a list of keys from the `_data/people.yml` file.
- `layout: project` This sets the layout of the actual project page. It should be set to `project`.
- `image:` The URL of an image for the project. This is shown on both the project page and the project card. Optional.
- `last-updated:` Date in the format of `YYYY-MM-DD`. The project cards are sorted by this, most recent first.
- `status: inactive` Set this to `inactive` if don't want the project to appear on the front page. Just ignore it otherwise.
- `link:` Set this to an external URL if this project has a page somewhere else on the web. If you don't have a `link:`, then the content of this markdown file (below the YAML frontmatter) will be this project's page.
- `no-link: true` Set this if you just don't want a project page for your project.

## Personnel

People are listed in a [YAML][] file in `_data/people.yml`. You can list the name, link, bio, and role of each person. Roles (e.g., "Faculty", "Staff", and "Students") are defined in `_config.yml`.

[YAML]: https://en.wikipedia.org/wiki/YAML


## Deploying to Your Sever

*For Mac/Linux:*
To set up deployments, edit the Makefile and look for the lines where `HOST` and `DIR` are defined. Change these to the host where your HTML files should be copied to.

To upload a new version of the site via rsync over ssh, type `make deploy`. A web hook does this automatically when you push to GitHub. Be aware that the Makefile is configured to have rsync delete stray files from the destination directory.

[Jekyll]: http://jekyllrb.com/
