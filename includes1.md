---
title: References in includes
permalink: includes1.html
layout: default
summary: "This Jekyll example was made to demonstrate and test Vladimir's Markdown Navigator plugin for IntelliJ. We will use out of the box Jekyll functionality for this."
---

## Includes of references

The links on this page where not created in the original markdown file but included via the liquid templating system. 

```text
WIth liquid “functions” are simply files, typically with the extension .html, in the site _includes directory (or a subdirectory of that folder). These can contain any HTML, markup, or Liquid code.
```

When refactoring a Jekyll website it would be great if the references in the includes are also refactored.

* Challenge: the includes file is in the _includes folder so the paths needed are different than they are needed in the actual files they are included in.

So now we included all the references and now we have them automatically available on each page and can create links to those pages easily:

* [Home] - Go to the homepage
* [Example 1] - This example
* [Example 2] - Source in path, target in root example
* [Example 3] - Both source and target in the paths example

One nice to have (not really necessary since refactoring doesn't take place a lot in the includes, it's a fixed directory and the filenames are rather straightforward, but it might come in handy with other liquid templating tags):

```text
the used liquid tag: { % include links.md % } 
```

* also refactor filenames between liquid tags
* One of the challenges here is that the 'include' command implicitly tells that the file is in the _includes folder




{% include links.md %}