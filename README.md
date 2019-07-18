# Foundation for Public Code Jekyll Theme

[![Build Status](https://travis-ci.org/publiccodenet/jekyll-theme.svg?branch=master)](https://travis-ci.org/publiccodenet/jekyll-theme)

A jekyll theme for the set up of quick generic static sites and for use with GitHub pages.

## Building locally

This theme is built to run predictably on GitHub pages, therefore the [`github-pages`](https://github.com/github/pages-gem) gem is required. Run `bundle install` before building with Jekyll.

To serve locally with Jekyll, use `bundle exec jekyll serve`.

## Customising

### Table of contents

#### For your whole site

You can turn on the display of Table of Contents ('On this page' section) for any page by adding `toc: true` to the `_config.yml` 

#### For just a specific page

Or adding `toc: true` to the front matter of any page where you want the Table of Contents to display.

### Breadcrumbs

You can turn on breadcrumbs for every page on the site by adding `show_breadcrumbs: true` to the `config.yml`.

Will result in breadcrumbs like:

> Main index.md title > grandparent index.md title > parent index.md title

:warning: Performance hit: since for every breadcrumb the partial needs to find the indexes and titles this will likely add quite a bit of time to the generation of your site.

### Metadata

Metadata for posts is to be displayed next to it if available, you can add metadata by adding front-matter like so:

```markdown
---
type: Guide
explains: something or other to put in this text here or there or everywhere wherever it makes sense
author: Ben
audience: Everyone
expires: 2019-04-22
bpmn: process.bpmn
---
```

The `expires` date is rendered by javascript and will highlight when expired.

The `bpmn` takes a filename and will draw a BPMN diagram.

### Foundation for Public Code footer

You can remove the footer with the contact information and higher level navigation to the footer by setting `hide_foundation_footer: true` in the `_config.yml`.

### Navigation

⚠️ This feature is experimental and might be removed.

You can turn on the navigation by adding `show_navigation: true` to the `_config.yml`. The position of items can be set on  the `order` property in the front-matter or in the `_config.yml`, and whether a page displays can be set by setting `hidden: true`.

## Licence

© Foundation for Public Code 2018

The code in this repository is licensed under [EUPL 1.2](LICENSE.md).

Logos, brands and trademarks of the Foundation for Public Code are licensed differently, check out https://brand.publiccode.net/ for more information.
