+++
title = 'This Page'
date = 2024-06-08T15:11:22-07:00
draft = false
+++

## What is this?

This is my blog page where I might or might not post interesting stuff that I have learned through my time.

### Building process

I build this page with [HUGO](https://gohugo.io/), a framework that offers a diverse set of templates to create a page of your own. I got a domain from [porkbun.com](https://porkbun.com) and then hosted using [GitHub](https://github.com/) pages.

Everything is very straightforward, after downloading the [dependencies](https://gohugo.io/installation/windows/#prerequisites), which is only, Go and the [HUGO](https://gohugo.io/) framework itself.

I installed the HUGO framework by [Chocolatey](https://chocolatey.org/) and ran the command

``` CLI
choco install hugo-extended
```

after this and of course with git pre-installed I ran a command

``` CLI
hugo new site YOUR SITE NAME
cd quickstart
git init
git submodule add "YOUR THEME REPO"
echo "theme = 'THEME NAME'" >> hugo.toml
hugo server
```

It is important to mention that sometimes the line

``` CLI
echo "theme = 'THEME NAME'" >> hugo.toml
```

Does not work, because for some reason the console will take the symbol ' as a Unicode symbol, and it will write trash in the created file, so manual modification is required. Just write inside the ``hugo.toml`` file ``theme = 'THEME NAME'`` inside, obviously replace "THEME NAME" with the name of the theme you are using.

### Creating posts

Creating a post in HUGO is as easy as creating the file. Content in HUGO works with markdown files which later are translated by HUGO to HTML.

You only need one command, and know [markdown](https://www.markdownguide.org/), which is very intuitive. I know pretty sure that LaTeX is also [supported](https://gohugo.io/content-management/mathematics/) but is something that I have not tried.

To start a new post the command is

``` CLI
hugo new create content/myPost.md
```

There's also different tags that you can use to make your posts more customized. It is nessaary to mention that the post will now show on your page until you set ``draft = true`` to ``false`` or you can have your post as a draft and run

``` CLI
hugo server -D
```

### That easy?

And that's it, this is how you can create a page like this or like my [resume page](armando.ooo) with basically only markdown and maybe LaTeX, but other knowledge is not necessary.

Building pages with HUGO is not a skill that will give you a job or something similar, is just something that could save you time and effort if your goal is just to show off your resume, or post silly things with a more customizable suit.
