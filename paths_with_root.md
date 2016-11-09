---
title: Using files in paths, but all generated html is published in root
permalink: paths_with_root.html
layout: default
summary: "This Jekyll example was made to demonstrate and test Vladimir's Markdown Navigator plugin for IntelliJ. We will use out of the box Jekyll functionality for this."
---

##   Our original files are in paths, generated HTML is in root
 
 This situation is achieved simply by using permalinks without a path:
 
```yaml
permalink: published_in_root.html
```

But my published_in_root.md file is in the path /pages/example4/. So my reference would look like this:

```markdown
[Example 4]: (/pages/example4/published_in_root.md)
```

Now we have the permalink and the reference basically pointing to the same file, but during writing with Jekyll the reference is correct and after publishing the permalink is correct. And when one is refactoring it would be great if both were refactored correctly.

Now the link [Example 4] is not working in the Jekyll published site because the end-result is not located in the path of the reference

[Example 5] link is working in the published site, but not in the plugin because the file is stored in the pages directory

[Example 4]: /pages/example4/published_in_root.html
[Example 5]: published_in_root.html
