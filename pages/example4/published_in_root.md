---
title: Original file in /pages/../.. the published file in root (because of permalink)
permalink: published_in_root.html
layout: default
summary: "This Jekyll example was made to demonstrate and test Vladimir's Markdown Navigator plugin for IntelliJ. We will use out of the box Jekyll functionality for this."
---

## This file sits in /pages/example4/ but is published in the root

The following links are created with the references included in the links.html

* [Home] - is working because this file and target are in root
* [Example 1] - also working 
* [Example 2] - also working
* [Example 3] - and working


{% include links.html %}