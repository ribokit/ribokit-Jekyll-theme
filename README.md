# RiboKit Theme for Jekyll

<img src="thumbnail.png" alt="Leap Day" align="right">

Inspired by the `2.0` version used by _GitHub Pages_, this theme is forked and modified from [**mattgraham/leapday**](https://github.com/mattgraham/leapday), used by https://ribokit.github.io and https://t47io.github.io.

## Installation

Please follow the following steps:

* Copy the `_includes`, `_layouts` and `assets` folders into the root directory of your new **Jekyll** project.

* Copy the `_config.yml` into the root directory of your new **Jekyll** project. Then edit the _Site settings_ section to your values.

* Test run with:
```bash
jekyll serve -w
```

## Documentation

Varibles available in the [**Front Matter**](https://jekyllrb.com/docs/frontmatter/) block are described in detail below (or see at https://ribokit.github.io/std/#jekyll):

In your **.md** file, use a header like this:

```go
---
layout: docs
permalink: /HiTRACE/tutorial/bonus_2d/
root: /HiTRACE/
prev: ../../biers/varna/
next: bonus_3d/

title: HiTRACE
description: "<u>Hi</u>gh-<u>T</u>hroughput <u>R</u>obust <u>A</u>nalysis for <u>C</u>apillary <u>E</u>lectrophoresis"
repo: hitrace/HiTRACE
author: Siqi Tian
---
```

* **System Fields**:

| Key | Value |
| --- | --- |
| `layout` | The layout template for the page. Choose from `default` (landing page for each package) and `docs` (leaf level page with navigation buttons). |
| `permalink` | The URL that the page responds to. Always start and end with `/`. |

* **Descriptive Fields**:

| Key | Value |
| --- | --- |
| `title` | The display title for the page. It will be displayed after the "RiboKit :" prefix; before the "\| RiboKit" suffix in browser title. |
| `description` | The subtitle for display. For acronyms, mark the initials with `<u>` for highlighting (on hover). |
| `repo` | The repository name in format of `organization/repository`. This powers the "View on GitHub" and "Download" buttons. If left out, those buttons are hidden. |
| `author` | The creator of the page. It will be displayed in the footer. |

* **Navigation Fields**:

| Key | Value |
| --- | --- |
| `root` | The root parent of the page. This will be used by the _up arrow_ button. |
| `prev` | The previous page, used for tutorial series. This will be used by the _left arrow_ button. The final (relative) URL is prepended with `../` (so you don't need to type it). |
| `next` | The next page, used for tutorial series. This will be used by the _right arrow_ button. The final (relative) URL is prepended with `../` (so you don't need to type it). |

## Credits

Created by [**t47**](http://t47.io/), *April 2016*.

Creative Commons Attributes: [**CC BY 3.0**](http://creativecommons.org/licenses/by/3.0/)
