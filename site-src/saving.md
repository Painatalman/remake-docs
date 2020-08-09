---
layout: layout.hbs
title: How Saving Data Works - Remake Framework Docs
---

## How Saving Data Works in Remake

1. Data is always [deep extended](https://davidwalsh.name/javascript-deep-merge), so overwriting data unnecessarily is always avoided
2. If you attach the `data-o-key-id` attribute to an element (with the attribute value set to a unique id that's auto-generated for every nested object in your database), then, when that element's data is modified, it's data will be saved directly to the unique id specified in that attribute
3. When data is deep extended, Remake always extends arrays by matching the unique ids of its child objects, so the data in deeply-nested arrays is preserved and never overwritten completely