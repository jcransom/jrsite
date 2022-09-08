# Blog integration process

0. Keep or retire?
1. Lead
2. Tags
3. Images (and captions)
4. Internal links

# Internal link (il)

[publication]({{< ref "publications/name" >}})

# New publication (np)

---
title: 'TITLE'
date: 14 Oct 2022
draft: false
showReadingTime: false
places: ['UK']
projects: ['Yorkshire']
types: ['Report']
externalUrl: 'url'
summary: 'This'
---

{{< alert "link" >}}
[Available here](url) (external link, PDF).
{{< /alert >}}

This

# Images

![James Ransom](author.jpg "James Ransom")

![alt](images/wine.jpg "Photo credit: [Unsplash](https://unsplash.com/photos/rFOrSRlkno0)")

# Alert

{{< alert "circle-info" >}}
Just looking for an example of my research? [Check out some samples]({{< ref "samples" >}}).
{{< /alert >}}

# Lead

{{< lead >}} Research. {{< /lead >}}

# YAML tags

places:
projects:
summary: 