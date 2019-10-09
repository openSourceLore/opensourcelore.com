---
title: "About"
permalink: /about/
layout: page
---

## What is Open Source Lore?

The goal of Open Source Lore is actually fairly simple: use the values and
ideals of the open source community to create a blog for anyone and everyone.
We'll follow git best practices to create discourse on any topic under the sun.
This site will also serve as an interesting experiment on what kinds of ideas
and opinions will be attracted to an open source microphone.

If you have written an article you want to share, or if you want to make any
changes to the site itself, send us a pull request
[here](https://github.com/openSourceLore/opensourcelore.com/pulls)! You can find
more information on contribution process below.

## How does it work?

It's fairly simple actually:

* We have an organization setup on GitHub, named
  [openSourceLore](https://github.com/openSourceLore), which houses our team of
  maintainers and the source code for the site.
* We have a repository within said organization, named
  [opensourcelore.com](https://github.com/openSourceLore/opensourcelore.com),
  which holds our GithHub Pages hosted site built with
  [Jekyll](https://jekyllrb.com/).
* We have a Google Domain for opensourcelore.com purchased and managed by
  GitHub user [learnitall](https://github.com/learnitall), the original founder
  of opensourcelore.com.

That's about it! Oh, we also use [mmistakes](https://github.com/mmistakes/)'s
[So Simple](https://github.com/mmistakes/so-simple-theme/) Jekyll theme, which
creates the awesomely simple look and feel for the site, and our logo was
created by [pixabay.com](https://pixabay.com) user
[openclipart-vectors-30363](https://pixabay.com/users/openclipart-vectors-30363/).

## What are the Contribution Guidelines?

The term "guidelines" can fall under two buckets: (1) best practices and (2)
how-to. We'll talk about each of these separately below:

### Best Practices

The maintainers at opensourcelore.com want to ensure that you have the freedom
to express yourself in every capacity, however there are some important ideas
to keep in mind when doing so:

1. **Avoid hate**. "Hate" can be interpreted in many different ways so let's
clarify. We *want* you to be able to express your opinions even if they are
going to upset somebody. There is a huge grey area in that statement alone, and
whether or not an article is acceptably appropriate to be posted on
opensourcelore.com will be left up to the discretion of the maintainers.
That being said, it is our responsibility to stomp out all forms of offensive,
crude and unproductive "junk" that only serves to tickle the fancy of the author.
This means we will not tolerate online hate speech. You can read more about
what is defined as online hate speech
[here](https://en.wikipedia.org/wiki/Online_hate_speech). Maintainers will do
their best to check all content that flows through the site during the pull
request process, but if you have a problem with an article on our site please
reach out to [stomp@opensourcelore.com](mailto:stomp@opensourcelore.com) and we
can take a look.
1. **Avoid Plagiarism**. Some types of articles are fact and information heavy.
For these types of articles, it is considered very appropriate, nice even, to
cite your sources, *always*. We understand that after heavy research some
sources of information can get lost, it happens to the best of us, but our goal
here is to support all content creators and readers alike. Try your best and
remember that the more links to other pages you can provide in your article, the
more information your readers will receive on the topic they are researching.
Let's try and help one another out. This means that, as a couple rules of a
strong thumb:
  * If it's not yours, don't claim it as your own.
  * If you used another site as a source of information for your article,
    include a link to that original piece of content. This could be in the form
    of a hyperlink, a "Works Cited", etc.
1. **Tag and Categorize Your Content**. Each article has an associated category
and tags which will help search engines find and provide your content. The more
accurately you can categorize and tag your article, the higher chance it has of
being found. Feel free to be unique in which tags and which category you choose-
go for existing tags and categories if you think they are applicable or create
your own if you desire.

That's pretty much it in this regard. No length restrictions, not too many topic
restrictions or anything of that sort. Go nuts! If you want to write poetry
about picture frames, rants about pickles, reviews of rubber bands, be our
guest!

### How-To

As with all things open source, if you're going to get involved we want to make
sure you can do so as painless, or as painful, as possible. To start, here's what
the whole process should entail if you are adding a new article:

#### Adding a New Article

1. Install and setup Jekyll.
1. Clone our repository.
1. Create a new branch (name isn't important).
1. Develop your article, committing to your newly created branch and testing
   out how the post looks and feels using your own Jekyll setup.
1. When finished, merge your branch into master. Please disable fast-forward by
   adding the option `--no-ff` and have your commit message be `"Draft 0 of
   'Your Title Here' by 'Your Author Name Here'`. The goal here is to have one
   commit that explains that your article is being added into the master branch.
1. Submit a pull request

Within your pull request, here's everything we'll need from you:

* **(Required)** Your article, formatted in markdown, placed into the
  [_posts](https://github.com/openSourceLore/opensourcelore.com/tree/master/_posts)
  directory. The filename of your piece should be formatted as
  `YYYY-mm-dd-your-posts-abbreviated-title.md`. Please have at least the
  following front matter defined at the top of the file, but you can of course
  get crazy with it by adding header images and such:

```yaml
layout: post  # This layout should be the same everytime, "post"
title: "Your title here"
date: ISO 8601 formatted date
categories:
  - "Your chosen category here"
tags:
  - "Your chosen tag here"
  - "Your second chosen tag here"
  - ...
  - "Your nth chosen tag here"
author: "Your author name here"
```

> **What is front matter?** Front matter is a bit of YAML-formatted text
> placed at the top of your article which helps Jekyll turn your markdown file
> into a full-on page on the site.
>
> Oh and be careful: if you do decide to add a header image to your post and
> define it in your front matter, be sure to commit the image itself also. You
> can place it in the [assets/images/headers](https://github.com/openSourceLore/opensourcelore.com/tree/master/assets/images)
> directory.

* **(Required)** Your information as an author, formatted in YAML, placed into
  [_data/authors.yml](https://github.com/openSourceLore/opensourcelore.com/blob/master/_data/authors.yml).
  This bit will determine what information appears alongside your post as the
  post's author. Please try to add your entry into this file in lexicographical order
  You can go as simple or as crazy here as you want. Here's a couple examples:

```yaml
# Bare bones/minimum requirements
# Add author named "Example A"
Example A:
  name: Example A 
# Author Image
# Add author named "Example B"
Example B: 
  name: Example B
  # Need to also commit this image
  picture: assets/images/authors/example_b.jpg
# External profile links
# Add author named "Example C"
Example C:
  name: Example C
  # Again, would need to commit this image
  picture: assets/images/authors/example_c.jpg
  links:
    - title: "LinkedIn"
      icon: "fab fa-fw fa-linkedin"
      url: https://linkedin.com/in/example-c
    - title: "Github"
      icon: "fab fa-fw fa-github"
      url: https://github.com/example-c
    - title: "Email"
      icon: "far fa-fw fa-paper-plane"
      url: mailto:examplec@opensourcelore.com
```

> **What's with all that "fab fa-fw..." shit?** That is a [Font Awesome Icon](https://github.com/openSourceLore/opensourcelore.com/tree/master/_posts)
> declaration, which our amazing Jekyll theme, [so-simple](https://github.com/mmistakes/so-simple-theme/),
> supports. You can use any font awesome icon here that you'd like!

After you've pushed your pull request with all the above, the maintainers will
review your post, provide feedback, and we'll go from there!

#### Revising an Existing Article

For this, the process is pretty much the same:

1. Clone our repository.
1. Create a new branch.
1. Make your changes to your article.
1. Merge your branch into master, disabling fast-forward with the `-no-ff` option
   and using the commit message `"Draft x of 'Your Title Here' by 'Your Author
   Name Here'` where x is this iteration's current draft number. For instance,
   if this is the third draft of your article, `x=3`.
1. Submit a pull request.

#### Making Other Changes

If there are any other changes you'd like to make to the site outside of article
editing, then feel free to do so! Lot's of flexibility here- just follow the same
branching, merging, pushing process but please be sure to use pretty commit messages.
Thanks!

#### One Last Important Note

To see all the possibilities that you have at your disposal while adding an article,
please view the documentation for our site's theme, [so-simple](https://github.com/mmistakes/so-simple-theme/),
and for [Jekyll](https://jekyllrb.com/docs/posts/) in general. If you have any
questions, please feel free to raise an issue in GitHub or send us an email at
[ihaveaquestion@opensourcelore.com](mailto:ihaveaquestion@opensourcelore.com).

