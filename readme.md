Test notes 2

## File Structure

`_posts`: This folder hosts files with our main content/blog for information. Any blog posts are stored here.

`_site`: Final output of website, when building the content the images, blog posts etc we use other folders. But when we have to host a website, all the static files these files go. The finished final version of my website. **Don't touch this**

`_config.yml`: (k-v pairs) Settings for jekyll website. Attributes about the site

`Gemfile`: Used with Ruby, to store dependencies for hosting the website.

## Frontmatter

Let's call it the meta of the page, or basically something we can use for jekyll. We store information about our pages using this or stuff like title, date etc. 


```
The below format denotes what the frontmatter looks like

---
title: MYTITLE
data: YYYY-mm-dd
layout: page
---

.... mycontent

```

It can be either YAML or JSON

### Permalink

Permalink is a way to modify the annoying urls generate for the blogs. It sets a permenent link to the whichever page holds the frontmatter for the page. 

accessing variables in permalink

`permalink: /:categories`

The above frontmatter uses the categories variables



## Posts

All files are under `_posts`

The url to the blog post of jekyll website is `domain/base_url/cat{in front matter of post}/date{frontmatter}/title.html`

You can categorize posts by using the frontmatter tag "categories"

The posts can be organized and managed into separate directories, and this won't change the url of the page

### Writing drafts

Preparing newer posts but dont want it published, create a new directory `_drafts` and store the information in that folder. The content under this folder wont be served to the web-client under the regular deployed server `jekyll serve` but you need a special command to run the server `jekyll serve --draft`

Whenever a draft is stored a default date is given of the current date

## Pages

For pages like landing page, about page and so on.. 

This is very simple to make, basically any markdown file under the root directory of the project can used as a page. For example: the `cretoblog/about.md` is the about page which is just a markdown file with some frontmatter


## Theme: Minimal mistakes 

Add `gem themename` to Gemfile

Modify **_config.yml** theme to `theme: newthemename`

Make sure to check out the layouts for the new themes and you'll have to adjust the frontmatter accordingly

