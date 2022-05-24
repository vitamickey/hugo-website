---
title: "Hugo"
date: 2022-05-23T15:04:53+10:00
# weight: 1
# aliases: ["/first"]
tags: ["website", "hugo", "technology", "coding"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: true
# description: "Desc Text."
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
- make a stubs page https://www.mtsolitary.com/stubs/ https://www.mtsolitary.com/20210329232300-mt-solitary-stack/
- backlinks??? lol I have a death wish https://www.mtsolitary.com/20210329232300-mt-solitary-stack/
- a search with filters like hugo tania would be cool