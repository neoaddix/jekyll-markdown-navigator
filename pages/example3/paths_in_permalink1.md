---
title:      The original and published version of our target is in a path
permalink:  paths_in_permalink1.html
layout:     default
summary:    "This Jekyll example was made to demonstrate and test Vladimir's Markdown Navigator plugin for IntelliJ. We will use out of the box Jekyll functionality for this."
---


## Demonstrates source and target files in paths (using permalink)

* This files md files is located in /pages/example3/paths_in_permalink.md
* The published html file is also located in /pages/example3/paths_in_permalink.html
* That's because of: permalink: /pages/example3/paths_in_permalink.html

Because the target file is in a path and the links.html contains relative links, they stop working:

* [Home] - broken because the links are relative to current location
* [Example 1] - broken link
* [Example 2] - broken link
* [Example 3] - (this page = working)


{% include links.md %}