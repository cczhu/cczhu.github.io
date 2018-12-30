# Jekyll Notes
## A reference for future me

## Installation

To install Jekyll, go [here](https://jekyllrb.com/docs/installation/).

## Basic usage

To make a Jekyll project folder:

```
jekyll new myblog
```

To build a website into `_site/`, use:

```
bundle exec jekyll build
```

Bundling runs Jekyll with the build environment specified in your Gemfile 
(just doing `jekyll build` will run some default environment).

To run a server, do:

```
bundle exec jekyll serve --livereload
```

which will build the `_site/` and rebuild it whenever you make a change to the
project's files.

## Tutorials

- [Giraffe Academy](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB)
- Quick start:
    1. `jekyll new myblog`
    2. `bundle exec jekyll serve --livereload`
