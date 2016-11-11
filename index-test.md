---
title: Index
permalink: index-test.html
layout: default
summary: "This Jekyll example was made to demonstrate and test Vladimir's Markdown Navigator plugin for IntelliJ. We will use out of the box Jekyll functionality for this."
---

# Configuration of the plugin

## Link mapping

Since Jekyll's final output is in .html format it expects all link
addresses in your markdown files to have an .html extension, even though
your source files are all .md files. A link reference would look like:

```markdown
[to the index](index-test.html)
```

Since the Markdown Navigator plugin looks for markdown files (and not
html files) it becomes less usable when doing Jekyll projects.
Fortunately this is solved in the next release with
[link mapping:](https://github.com/vsch/idea-multimarkdown/wiki/Modifying-Link-Processing)

### Solution
The link mapping feature in the next release, already available on
the EAP update channel, can be used to change all the links to .html
during completions and to resolve .html link addresses to .md documents.
It can also be used to change path.

[Link mapping in practice](/assets/linkmapping_inpractice.gif)

So now it's possible to have .html extensions in the markdown, while working with markdown filenames. This is used in [Example 1]: 

* [Example 1] uses an **include file** for the references, refactoring
  should also work for the references in the links.html includes file
* [Example 2] uses pages that are **not in the root**, so source file names
  include a path, but the permalinks (target file) don't and the final
  html file is published in root by Jekyll (because the permalink says so)
* [Example 3] same as example 2 but now the **permalink also includes the
  full path** so the path of the source and target files are the same

Concerning the references on this page:

* When the .html extension is used (as Jekyll likes), the plugin can only create an .html filename if it does not exist yet. When the link mapping .md <-> .html is active it might be nice when you also get the option to create a new file that way. So in the code below there is an 'unresolved reference link' with the option 'create file new-file.html', but the user wants an .md file in this case (the original file is md, the reference is to the published html)

```
[create a new file]: new-file.html
-> when using the plugin to create the new-file it would be nice to be able to create the .md version of the file even though the links says html
```

[Example 1]: includes1.html
[Example 2]: paths_with_root.html
[Example 3]: pages/example3/paths_in_permalink1.html



    
    
    
    
