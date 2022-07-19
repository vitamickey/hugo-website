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
lastmod: 2022-07-16T22:48:53+10:00
---

I already have broken my website. 

I started with `hugo new post/so-it-began.md` to create my first post, and then tried to change the folder "post" to "posts", added a second file with `hugo new posts/digital-garden.md`, and now it's not showing up on my website. lol.

Thanks to this video for the setup guide tho https://www.youtube.com/watch?v=LIFvgrRxdt4. And I think I used https://janezhang.ca/posts/building-website-with-hugo/ for inspo.

I am a bit unnerved by the fact that he doesn't merge to the main branch via a pull request and instead commits straight to the main branch. I am 99% sure that is bad git practice. 

I started with the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, and then tried using PaperModX for a bit, and then decided to switch back to PaperMod because 1. I figured out how to better use Hugo and 2. PaperModX had too many bugs for me. 
To build my site, need to use `hugo -t PaperMod` (or instead of `PaperMod`, the current website theme).

I need to
- ~~add comments with Disqus https://gohugo.io/content-management/comments/~~
- make a stubs page?? https://www.mtsolitary.com/stubs/ https://www.mtsolitary.com/20210329232300-mt-solitary-stack/
- BACKLINKS??? lol I have a death wish https://gabrielleearnshaw.medium.com/implementing-backlinks-in-a-hugo-website-e548d3d8f0e0 https://www.mtsolitary.com/20210329232300-mt-solitary-stack/ 
- a search with filters like hugo tania or Maggie Appleton's website would be cool https://gohugo.io/content-management/taxonomies/ https://gronskiy.com/posts/filtering-posts-over-multiple-taxonomies-hugo/
    - an option to see my posts related to any book of the bible, maybes
    - also don't generate pages for these?? I would just want to be able to filter through tags and such, don't need a page per tag or anything
- ordering by last tended, not by date planted
- proper implementation of horticultural extended metaphor ?? or figure out my own metaphor (but plants are nice)
- add relative dates to meta https://kodify.net/hugo/date-time/relative-age-hugo/
- ~~make maths work on the site AAAAA~~
- ~~increase list indentation~~ 
- ~~if I make sublists there's like additional spacing below the last one~~
    - a bit
        - like this here
    - this ^, so I need to figure out what's going on
    - r.e. above I figured it out but like it's not quite fixed, but I made the `ul, ol` thingos with `margin = 16px`, i.e. font size of website, and it did happy things.
    - OK with brute force I think I fixed it finally so  NICE thanks to https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Styling_lists
- side-by-side images?? I try the https://discourse.gohugo.io/t/putting-image-side-by-side/3926 solution but there might be something in my CSS that botches this up.

<!-- 1. let's
    1. fix
        1. this
        2. issue
    2. today
    3. like now
2. because
3. it is
4. annoyings

what is happening

- let's
    - fix
        - this
    - issue
    - today
- because
- it is
- annoying -->

To customise CSS and HTML of a theme, you should **override** these rather than edit the themes files directly. The PaperMod files of my website were downloaded onto my laptop and edited directly, which I shouldn't have done. For HTML, images, etc., you can create a new file in the folders of your actual site, rather than the theme's folders. For example, to overwrite `head.html` stored in `/my-site/themes/theme-name/layout/partials/` you can copy that file into something like `/my-site/layouts/partials/` and then the content of that file will overwrite the original file. This is especially important if you have cloned a repository (but that's kinda of obvious, right?). To do that but for CSS, I am referencing Banjo Code. 

https://www.banjocode.com/post/hugo/custom-css/

Had to do this too
https://stackoverflow.com/questions/65040931/hugo-failed-to-find-a-valid-digest-in-the-integrity-attribute-for-resource

Did this
https://bphogan.com/2020/08/11/2020-08-11-creating-unlisted-content-in-hugo/

Changed markdown to render HTML with https://gohugo.io/getting-started/configuration-markup/ by changing goldmark renderer to `unsafe = true`
