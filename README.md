# RiboKit Theme for Jekyll

<img src="thumbnail.png" alt="Leap Day" align="right">

Inspired by the `2.0` version used by _GitHub Pages_, this theme is evolved from [**mattgraham/leapday**](https://github.com/mattgraham/leapday), used by https://ribokit.github.io.

## Installation

Please follow the following steps:

* Copy the `_includes`, `_layouts` and `assets` folders into the root directory of your new **Jekyll** project.

* Copy the `_config.yml` into the root directory of your new **Jekyll** project. Then edit the _Site settings_ section to your values.

* Copy the `404.html` into the root directory. This is a custom 404 page.

* Test run with:
```bash
jekyll serve -w
```

<hr/>
## Documentation

### Front Matter

Varibles available in the [**Front Matter**](https://jekyllrb.com/docs/frontmatter/) block are described in detail below (or see at https://ribokit.github.io/docs/jekyll/):

In your **.md** file, use a header like this:

```go
---
layout: docs
permalink: /HiTRACE/tutorial/bonus_2d/
root: /HiTRACE/
prev: /Biers/varna/
next: ../bonus_3d/

title: HiTRACE
description: "<u>Hi</u>gh-<u>T</u>hroughput <u>R</u>obust <u>A</u>nalysis for <u>C</u>apillary <u>E</u>lectrophoresis"
repo: hitrace/HiTRACE
author: Siqi Tian
---
```

> Remember that all URL path (`permalink`, `root`, `prev`, `next`) are **CASE SENSITIVE**. Use spellings that match the actuall repository name!

* **System Fields**:

| Key | Value |
| --- | --- |
| `layout` | The layout template for the page. Use `default` for all pages; use `redirect` for redirecting a `permalink` to a new address (with a 301 page, see `redirect_to`). |
| `level` | The level for the page. This controls the navigation banner: `0` displays "Visit Lab" button; used for domain index page only (e.g. `https://ribokit.github.io`). `1` displays "View GitHub" and download package for repository; used for landing page of each package (e.g. `https://ribokit.github.io/RiboVis/`). `2` displays "up", "prev", "next" navigation buttons; used for tutorial series (e.g. `https://hitrace.github.io/HiTRACE/tutorial/step_0/`). |
| `permalink` | The URL that the page responds to. Always start and end with `/`. |

* **Descriptive Fields**:

| Key | Value |
| --- | --- |
| `title` | The display title for the page. It will be displayed after the "RiboKit :" prefix; before the "\| RiboKit" suffix in browser title. |
| `description` | The subtitle for display. For acronyms, mark the initials with `<u>` for highlighting (on hover). |
| `repo` | The repository name in format of `organization/repository`. This powers the "View on GitHub" and "Download" buttons. If left out, those buttons are hidden. |
| `author` | The creator of the page. It will be displayed in the footer. |
| `ga_tracker` | Google Analytics tracker ID. This should only be set once globally as defaults. |

* **Navigation Fields**:

| Key | Value |
| --- | --- |
| `root` | The root parent of the page. This will be used by the _up arrow_ button. |
| `prev` | The previous page, used for tutorial series. This will be used by the _left arrow_ button. Your relative or absolute path/URL is used as is. |
| `next` | The next page, used for tutorial series. This will be used by the _right arrow_ button. Your relative or absolute path/URL is used as is. |
| `redirect_to` | New address to redirect a page. Only works when `layout` is `redirect`. Either relative or absolute path works. |

Example of link redirection:

```go
---
permalink: /biers/
redirect_to:  https://ribokit.github.io/Biers/
---
```

### Defaults

Within the same package, the `title`, `description`, `repo`, `root`, _etc._ are usually the same across all pages. In the `_config.yml`, you can define default values globally:

```go
defaults:
  -
    scope:
      path: ""
    values:
      layout: "default"
      level: 1
      title: 
      author: "Siqi Tian"
      ga_tracker: UA-12345678-9
```

> The settings are global when `path: ""` is empty.

Also, you can define defaults for a package:

```go
defaults:
  -
    scope:
      path: "repos/ribovis"
    values:
      title: "RiboVis"
      description: "PyMol Commands by the Das Lab Style"
      repo: "ribokit/RiboVis"
      author: "Siqi Tian"
      root: "/RiboVis/"
```

Now for your individual **.md** files, you don't need to repeat the default variables.

<hr/>
## Credits

Created by [**t47**](https://t47.io/), *April 2016*.

Creative Commons Attributes: [**CC BY 3.0**](http://creativecommons.org/licenses/by/3.0/)
