# kristinarusimova.github.io
Personal website

## Adding content

### Add a top-level page

* Create a new file in `_pages`
* Add front matter to the top of the file, and ensure the front-matter includes `nav: true`
    * See other pages such as `publications.md` for an example

#### Example page content

```
---
layout: page
permalink: /test/
title: Test
nav: true
---

Test page content
```

### Adding a sub-page (e.g. projects, teaching, etc.)

* Create a new file in `_projects`
* Add a thumbnail image to the `assets/img` folder
* Add front matter to the top of the file, and ensure the front-matter includes:
    * `location`
    * `img` (relative path to the image you just added to assets)
    * `importance` (integer to detemine order of projects)
    * `years` (years the project was active) 

#### Example page content

```
---
layout: page
title: A new project
description: >
    Blah blah bah this is a project description
location: University of Bath
img: /assets/img/secret.png
importance: 2
years: 2021-2022
---

Project page content
```
