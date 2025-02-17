---
layout: default
title: Writing guide
permalink: /writing-guide/
nav_exclude: true
description: "A guide to writing content on this working in the open site."
---
#  Writing guide
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Aims of working in the open

Our goal is to show the W3C community how we're working on the W3C website redesign project and to share progress.

We aim to publish content to the working in the open site frequently, where possible on a weekly basis.

Studio 24 will continue to prepare project docs in tools such as Basecamp, Google Docs, InVision, etc. As soon as these 
are ready to share with the W3C team we will publish these to this site, even if they are draft or work-in-progress. This 
also makes it easier to share with the wider W3C project review team who do not have direct access to Basecamp.

If there is a genuine need to only share private docs with the immediate W3C project team we will do so via Basecamp.

All site updates will be added to the timeline. These appear automatically on the homepage, timeline page and RSS feed. 

## Deployment
We use [Netlify](https://www.netlify.com) to build and host the working in the open site.

Any changes to the `main` branch are automatically deployed by Netlify and published to the live site at
[https://w3c.studio24.net/](https://w3c.studio24.net/)

If you create a Pull Request a preview URL is automatically generated by Netlify and available to review your work (see 
link on the Pull Request page).

## Editing content

### Markdown files

Content is written in [Kramdown](https://kramdown.gettalong.org/quickref.html) markdown formatting. You can 
[learn how to write markdown](https://lab.github.com/githubtraining/communicating-using-markdown).

## Adding content

You need to add any new content to a branch, make your edits there, and raise a Pull Request to request to merge changes 
into the main default branch.

* [w3c-website-redesign-documentation git repo](https://github.com/w3c/w3c-website-redesign-documentation)
* [Proposing changes to your work with pull requests](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests)
* [Creating and deleting branches within your repository](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-and-deleting-branches-within-your-repository)
* [Creating a pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)
* [Merging a pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/merging-a-pull-request)

## Add all site updates to the timeline

The timeline acts as a list of all updates made to this site. Please add a timeline entry for all new content additions 
and any content changes (e.g. an updated document).

You can edit this in the `_data/timeline.yml` file. 

Each timeline update must contain:

* `title` - short title for this update (try to keep this under 8 words)
* `date` - date this update happened (not the date you publish this update to the site)

Each timeline update may contain:

* `link` - link to further information, for example a document or update post. It's also OK to link to external resources here such as InVIsion or Google Docs. Just make sure the links are publicly accessible.
* `description` - an optional longer description. If you don't include a link you must include a description (one of these is required for the RSS feed) 

## Types of content

### Pages

Content pages on the site. 

#### Front matter

* `layout: default` - layout template
* `title` - page title
* `permalink` - the page URL (use start and end slashes) 
* `nav_order` - display in primary nav in this order
* `nav_exclude` - do not display in primary nav, e.g. `nav_exclude: true` 
* `description` - short description of the page 

Example:

```
---
layout: default
title: About Studio 24
permalink: /about-studio24/
nav_order: 7
description: "An introduction to Studio 24 and the team working on this project."
---
```

### Docs

Project documents. We should publish these as soon as we want to share these with the wider W3C team & community. 

#### Front matter
{: .no_toc }

* `layout: doc` - layout template
* `title` - page title
* `date` - date (YYYY-MM-DD) document was shared with W3C
* `updated` - date (YYYY-MM-DD) document was last updated on working in open site (optional)
* `categories` - list of categories separated by comma
* `description` - short description of the page
* `author` - the people who wrote the document 
* `thumbnail` - Thumbnail image, used for social sharing  
* `thumbnail_alt` - Alternative text for thumbnail image

Example: 
 
```
---
layout: doc
title: "Front end standards"
date: "2020-06-12"
updated: "2020-06-30"
categories: [Planning]
description: "The front-end standards we plan to use within the W3C website redesign project are summarised below. Further details on each item appear in this document."
author: Carlos Eriksson, Nicola Saunders
thumbnail: "/assets/images/img-standards.png"
thumbnail_alt: "Sketch of an American Football Placekicker scoring a field goal. The football shows the W3C logo. 'Standards' is written in the end zone."
---
```

#### Draft docs
{: .no_toc }
It's OK if these documents are work-in-progress or draft, just note this in the document title and timeline title. E.g.

```
title: Information architecture report (draft)
```

### Updates

Occasional project update posts that are not project documents go here. Think of these as project posts or short updates.

#### Front matter
{: .no_toc }

* `layout: post` - layout template
* `title` - page title
* `date` - date (YYYY-MM-DD) document was shared with W3C
* `categories` - list of categories separated by comma
* `description` - short description of the page
* `author` - the people who wrote the document 
* `thumbnail` - Thumbnail image, used for social sharing  
* `thumbnail_alt` - Alternative text for thumbnail image

