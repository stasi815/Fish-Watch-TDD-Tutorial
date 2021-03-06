# Tutorial Template

This is the template to be used for Make School tutorials hosted on makeschool.com. Use this repository as a starting point for your tutorial. Each tutorial must follow it's file structure and include all files included in this repository.

If you have a specific question, feel free to use the table of contents to skip to the area you're looking for:

| Folder/File   | Description |
|:--------------------|:-----------------------|
| [README.md](README.md) | Learn how to structure your tutorial repository so that it renders correctly on MakeSchool.com |
| [P00](P00-Getting-Started/content.md) | Learn syntax for writing tutorials that utilizes the special Make School markdown syntax  |
| [P01](P01-First-Chapter/content.md) | Learn how to write the first chapter of a tutorial, which should have a similar format regardless of topic/course |
| [P02](P02-Writing-Content/content.md) | Learn in general how to write out the rest of the tutorial, such as best practices and required sections (i.e. git commits, tests, etc.) |

In this tutorial template, we will discuss best practices for creating Make School tutorials. We'll cover:

1. Development tools needed to write tutorials
1. Tutorial  repository structure
1. Supported syntax
1. How to write the first chapter of a tutorial
1. How to write/pace the content throughout your tutorial

# Set Up

Before starting, make sure you have the following tools installed and ready in order to successfully write/edit/preview your tutorial

## Development tools

1. Install [Atom](https://atom.io/) for writing tutorial markdown. We use Atom because we have a custom Atom plugin to help render Make School specific markdown syntax
1. Add the [ms-markdown-preview](https://github.com/makeschool/ms-markdown-preview) package. **Contact Dion if you do not have access to this repository.**
1. Read the Notion page on [Creating, Editing, and Adding Tutorials and Tracks to the Website](https://www.notion.so/makeschool/Creating-Editing-and-Adding-Tutorials-and-Tracks-to-the-Website-bd69d5a60b074344a792eee48f12f02e). This covers the previous setup items, but also says how to edit/upload tutorials to makeschool.com
1. Read the [How to Fix Tutorials](https://drive.google.com/open?id=1-xPt7RjGT6kTyuJO9SCcNAy_HPCMqugcwTSQ3Kh4iyY) and [How to Make a Tutorial](https://docs.google.com/document/d/1xZvADsA5bleIwMrhENRm3m-wcHKWZKv1CL9TTI4vJos/edit?usp=sharing) guides to get a sense of how we write tutorials at Make School.

Once installed, these tools will allow you to see how your tutorial will look on the website without having to import it. Always check the preview (`Cmd + ctrl + R`) before pushing changes to a tutorial!

# Tutorial repository structure

See the structure of this repository for the general tutorial structure. Each tutorial contains:

- `tutorial.yaml`, contains metadata for the tutorial
- Folders for each tutorial page
- `cover.png`
- .gitignore

## tutorial.yaml attributes

- `title` (56 characters maximum): a slug for the tutorial will be generated from title. The title must be unique from all other Make School tutorials.
- `cover`: local file reference to cover image name -- displayed when viewed from [/tutorials](https://makeschool.com/tutorials) and at the top of each tutorial page. Should always be named `cover.png` and placed at the root of the tutorial. Do not change this.
- `teaser_text` (150 characters maximum): displayed when viewed from [/tutorials](https://makeschool.com/tutorials).

# Tutorial chapter folder structure

Each folder represents a tutorial chapter and should contain the page `content.md` and an `assets` folder containing any assets the page needs.

## Naming tutorial page folders

The folders should be named with the format `P[page-number]-Page-Slug` where:

- `[page-number]` is a double digit number from `00` through `99` representing the page order
- `Page-Slug` matches the slug defined in the tutorial page's `content.md`

## content.md

Each page's content is defined using `Markdown` in `content.md`. The top of `content.md` has the format:

```
---
title: "Page Title"
slug: page-slug
---

...
```

where:

- `Page Title` becomes the first header and is used in the tutorial's table of contents
- `page-slug` is a unique (to the tutorial) slug representing the page's title
- `...` is the actual content of the tutorial page

### assets folder

All local assets (png, gif, zip, mov, mp4, etc) for a pages should be inside the `assets` folder. Give assets meaningful names and avoid using spaces. Be careful with asset sizes! Short screencasts can be local but host large videos on Youtube or S3.

## cms_id

Legacy files generated by the website importer. They should not be modified or copied from other repositories. Newly imported tutorials will not have these.
