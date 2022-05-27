---
# weight: 1
# aliases: ["/first"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: true
# canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: false
ShowPostNavLinks: true
ShowRssButtonInSectionTermList: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
# editPost:
#     URL: "https://github.com/vitamickey/digital-garden/tree/main/content"
#     Text: "Suggest Changes" # edit text
#     appendFilePath: true # to append file path to Edit link
date: 2022-05-23T15:04:53+10:00
title: "Hugo"
description: "What I use to make my site."
tags: ["website", "technology", "coding"]
lastmod: 2022-05-23T15:12:53+10:00
---

I already have broken my website. 

I started with `hugo new post/so-it-began.md` to create my first post, and then tried to change the folder "post" to "posts", added a second file with `hugo new posts/digital-garden.md`, and now it's not showing up on my website. lol.

Thanks to this video for the setup guide tho
https://www.youtube.com/watch?v=LIFvgrRxdt4

I am a bit unnerved by the fact that he doesn't merge to the main branch via a pull request and instead commits straight to the main branch. I am 99% sure that is bad git practice. 

To build my site, need to use `hugo -t PaperMod` (or instead of `PaperMod`, the current website theme).

I need to
- add comments with Disqus https://gohugo.io/content-management/comments/
- make a stubs page?? https://www.mtsolitary.com/stubs/ https://www.mtsolitary.com/20210329232300-mt-solitary-stack/
- BACKLINKS??? lol I have a death wish https://gabrielleearnshaw.medium.com/implementing-backlinks-in-a-hugo-website-e548d3d8f0e0 https://www.mtsolitary.com/20210329232300-mt-solitary-stack/
- a search with filters like hugo tania or Maggie Appleton's website would be cool
-- an option to see my posts related to any book of the bible, maybe
- ordering by last tended, not by date planted
- proper implementation of horticultural extended metaphor ?? or figure out my own metaphor (but plants are nice)
- add relative dates to meta https://kodify.net/hugo/date-time/relative-age-hugo/


To customise CSS and HTML of a theme, you should **override** these rather than edit the themes files directly. The PaperMod files of my website were downloaded onto my laptop and edited directly, which I shouldn't have done. For HTML, images, etc., you can create a new file in the folders of your actual site, rather than the theme's folders. For example, to overwrite `head.html` stored in `/my-site/themes/theme-name/layout/partials/` you can copy that file into something like `/my-site/layouts/partials/` and then the content of that file will overwrite the original file. This is especially important if you have cloned a repository (but that's kinda of obvious, right?). To do that but for CSS, I am referencing Banjo Code. 

https://www.banjocode.com/post/hugo/custom-css/