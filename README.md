
# Data Science Group - website

**Credits:** This project is based on the [repository](orig_repo) provided by the University of Washington. The website of the original creators can be accessed [here][sampa].

**License:** This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License][license].

[orig_repo]: https://github.com/uwsampa/research-group-web
[sampa]: http://sampa.cs.washington.edu/
[license]: https://creativecommons.org/licenses/by-nc/4.0/

--- 

## Features

* The website is based on Ruby and [Jekyll][]. Where the content is just text files edited using [Markdown language](markdown).
* The publications list is generated from the BibTeX file located in `bin/papers.bib`, using [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar).
* Personnel list. Organize your professors, students, staff, and alumni are modified from `_data/people.yml`.
* Combined news stream and blog posts.
* Easily extensible navigation bar.
* Responsive (mobile-ready) design based on [Bootstrap][].

[markdown]: https://www.markdownguide.org/basic-syntax/
[Bootstrap]: http://getbootstrap.com/

## To contribute to the website from your computer

1. Install [Ruby][] in your computer according to your operating system.
2. Then, install Jekyll and bundler through:
   -  ` gem install jekyll bundler`
4. Clone the fork to your own machine: 
   - `git clone https://github.com/dsv-data-science/dsv-data-science.github.io.git`
5. Access in the terminal to the folder `cd dsv-data-science.github.io`
6. Install the rest of the gems using: `bundle install`
7. Check that you use the `source` branch of the repo while development purposes. `master` is used for deployment of the static website and avoid CI/CD in GitHub (which does not support compilation of `.bib`).


[Jekyll]: http://jekyllrb.com/]
[Ruby]: https://www.ruby-lang.org/en/downloads/

## To edit or contribute to the website

1. Keep adding content. See below for instructions for each of the various sections. Create `_posts`, `_projects`, or research areas under `_research`
2. To start your local server to check how it would look like when deployed to the server.
   - `bundle exec jekyll serve`
3. The terminal will show an IP where the website is hosted. Usually `127.0.0.1:4000`
4. Finally, the website with the files to be pushed are in the folder `_src`.

**Note:** Remember to `git pull` before start editing and `git push` whenever your changes are done.

## Deploying to DSV Sever

After testing your local server, any contributor can update the website `dsv-data-science.github.io` by running the bash command `./bin/deploy`.

To deploy the website in the DSV server `datascience.dsv.su.se` please contact Panos (to request access to the server) or Luis Quintero (he will update the website with changes).

*Connection to the server:* 
- `HOST: mimas[dot]dsv[d]su[d]se`
- `ssh <HOST>`
- `PATH: /www/datascience`
- `cd <PATH>` and delete all files web files: `rm -r *`
- Copy the website files through SCP:
  - `scp -r _src/* [username]@mimas[dot]dsv[d]su[d]se:/www/datascience`

## Work to do
- Use `rsync` instead of `scp` and add commands to bash in `./bin/deploy`.
- Modify the projects and research templates with a table of contents on the right side of the page.

# Features details

Write your information with MarkDown language, images can be added to `/img/areas/` and referenced as:

```
![general]({{ site.base }}/img/areas/file.png){:width="50%"}
```

While writing your page, you can also use emojis 🥽, and text with inline $$\LaTeX$$ or a single centered formula (leaving an empty line between text and formula):

$$ \sum_{i=1}^{N}{i} = i \in \mathbb{R}^+ $$


## Publication List

The list of publications is in `bib/papers.bib`. These are compiled and grouped per year. If you want to make your publication clickable, add the web URL using the key `url = {},`, and to make the paper visible in the page of a specific research area use the key `keyword={}`, as follows:

|keyword|Area|
|---|---
|temporal|Searching and mining temporal data|
|healthcare|Learning from ECH|
|explainable|Interpretable and Explainable models|
|federated|Federated Learning|
|vehicles| Integrated Vechicle Management|
|nlp|Natural Language Processing|
|reinforcement|Reinforcement Learning|
|immersive|Immersive Technologies and VR|


Each co-author that is part of the group (edit in `_data/people.yml`) will have a link that point to their website (if specified).

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
