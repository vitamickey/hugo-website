---
date: 2022-05-23T15:04:53+10:00
title: "Hugo"
description: "What I use to make my site."
tags: ["website", "technology", "coding"]
lastmod: 2022-08-25
---

## Workflow

(sorry my terimnology may be all wrong when it gets to git-related things)

- editing
  - do whatever adding posts, changing taxonomies, etc.
  - test as needed with `hugo server -D` as necessary (loads site at `http://localhost:1313/` without comments to avoid duplicate Disqus entries as specified I think in my `comments.html` partial)
- when ready to update live site
  - empty `/public/` except for `.git` and `CNAME`
  - build static files with `hugo -t papermod`
  - do github things
    - create new branch for `public` submodule as `YYMMDD`
    - stage all changes
    - commit
    - publish branch
    - create pull request
    - merge with main
      - resolve any errors in VSCode if necessary (often with my clumsy coding skills is necessary)
    - delete branch on GitHub
    - delete branch locally on VSCode
    - checkout? to main branch and sync with remote main
  - repeat "do github things" with `digital-gardens` repo
  - check site is live
    - record any errors that may have happened

## To-do

I need to

- ~~add comments with Disqus <https://gohugo.io/content-management/comments/>~~
- make a stubs page?? <https://www.mtsolitary.com/stubs/> <https://www.mtsolitary.com/20210329232300-mt-solitary-stack/>
- BACKLINKS??? lol I have a death wish <https://gabrielleearnshaw.medium.com/implementing-backlinks-in-a-hugo-website-e548d3d8f0e0> <https://www.mtsolitary.com/20210329232300-mt-solitary-stack/>
- a search with filters like hugo tania or Maggie Appleton's website would be cool <https://gohugo.io/content-management/taxonomies/> <https://gronskiy.com/posts/filtering-posts-over-multiple-taxonomies-hugo/>
  - ~~an option to see my posts related to any book of the bible, maybes~~
    - ~~each book of the bible to have its own page that displays a list of all related notes and my own content written about it~~
  - also don't generate pages for these?? I would just want to be able to filter through tags and such, don't need a page per tag or anything
    - actually I may need to redact this, because it's kind of nice to have those since I cannot figure out backlinks for the life of me
- ~~ordering by last tended, not by date planted: I now know how to do this~~
- proper implementation of horticultural extended metaphor ?? or figure out my own metaphor (but plants are nice)
- add relative dates to meta <https://kodify.net/hugo/date-time/relative-age-hugo/>
- ~~make maths work on the site AAAAA~~
- ~~increase list indentation~~
- ~~if I make sublists there's like additional spacing below the last one~~
  - a bit
    - like this here
  - this ^, so I need to figure out what's going on
  - r.e. above I figured it out but like it's not quite fixed, but I made the `ul, ol` thingos with `margin = 16px`, i.e. font size of website, and it did happy things.
  - OK with brute force I think I fixed it finally so  NICE thanks to <https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Styling_lists>
- side-by-side images?? I try the <https://discourse.gohugo.io/t/putting-image-side-by-side/3926> solution but there might be something in my CSS that botches this up.
- blockquotes in lists
    > they do not play nice. I mean, look at that spacing? :(
- ~~footnotes bleed into meta[^1]. Due to poor placement of post meta~~
- ~~on that, I've been formatting footnotes incorrectly lol.~~
  - ~~Also, on notes like `judging-loving`, the meta spacing is influenced by spacing with the nav buttons. This was a result of poor placement of my post meta, but it's fixed now~~
- favicon broken when moved into a different folder under `static`
  - I have moved the site web manifest into the folder with the favicons, it wasn't there before
    - if this fixes it, I will revert changes I made in my `head.html` file as specified further below
  - next attempt at quick fix: move it back to where it was when it worked lol
- nested tags?? <https://dpb587.me/post/2020/03/09/nested-taxonomies-with-hugo/>
- css for code blocks (see end of page)
  - for different languages
    - text
    - html
    - css
    - latex
    - R
    - python
    - markdown
- Emoji support <https://www.markdownguide.org/extended-syntax/#emoji>

here is something else that isn't nice

- here is a list
  - and a subpoint
  - and another

- and when I put another list below it with a space
  - it's gonna get
  - kinda hairy because the spacing gets really weird between the parent and subpoint
- idk what to do
- here's me trying more stuff
  - and another indent

<!-- 1. let's
    1. fix
        1. this
        2. issue
    2. today
    3. like now
1. because
2. it is
3. annoyings

what is happening

- let's
    - fix
        - this
    - issue
    - today
- because
- it is
- annoying -->

## Changelog and lessons learned

I already have broken my website.

I started with `hugo new post/so-it-began.md` to create my first post, and then tried to change the folder "post" to "posts", added a second file with `hugo new posts/digital-garden.md`, and now it's not showing up on my website. lol.

Thanks to this video for the setup guide tho <https://www.youtube.com/watch?v=LIFvgrRxdt4>. And I think I used <https://janezhang.ca/posts/building-website-with-hugo/> for inspo.

I am a bit unnerved by the fact that he doesn't merge to the main branch via a pull request and instead commits straight to the main branch. I am 99% sure that is bad git practice.

I started with the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, and then tried using PaperModX for a bit, and then decided to switch back to PaperMod because 1. I figured out how to better use Hugo and 2. PaperModX had too many bugs for me.
To build my site, need to use `hugo -t PaperMod` (or instead of `PaperMod`, the current website theme).

To customise CSS and HTML of a theme, you should **override** these rather than edit the themes files directly. The PaperMod files of my website were downloaded onto my laptop and edited directly, which I shouldn't have done. For HTML, images, etc., you can create a new file in the folders of your actual site, rather than the theme's folders. For example, to overwrite `head.html` stored in `/my-site/themes/theme-name/layout/partials/` you can copy that file into something like `/my-site/layouts/partials/` and then the content of that file will overwrite the original file. This is especially important if you have cloned a repository (but that's kinda of obvious, right?). To do that but for CSS, I am referencing Banjo Code.

<https://www.banjocode.com/post/hugo/custom-css/>

Had to do this too
<https://stackoverflow.com/questions/65040931/hugo-failed-to-find-a-valid-digest-in-the-integrity-attribute-for-resource>

Did this
<https://bphogan.com/2020/08/11/2020-08-11-creating-unlisted-content-in-hugo/>

Changed markdown to render HTML with <https://gohugo.io/getting-started/configuration-markup/> by changing goldmark renderer to `unsafe = true`

In `head.html`, changed something about favicon stuff because I moved my favicon files elsewhere and my website does not like it so seeing if this fixes it.

```html
{{/*  <link rel="icon" href="{{ .Site.Params.assets.favicon | default "favicon.ico" | absURL }}">
-> <link rel="icon" href="{{ .Site.Params.assets.favicon | absURL }}">
```

Unsure how to nest functions in hugo yet.

Added URLS to the books of Bible overview pages so that instead of `/46-1-corinthians/` being the end of the URL, it's just `/1-corinthians/` <https://gohugo.io/content-management/urls/>. Doesn't cause clashes with `/booksofbible/1-corinthians/`.

Actually, now I've changed it so that `/1-corinthians/` links to a page that displays every page that hasthe `1-corinthians` term in the `booksofbible` key, and I've added a custom `_index.md` to each directory `\content\booksofbible\BOOKNAME\` so that I can put my overview of each book of the bible there. I think chapters of the bible would make it too messy, but I think I could try and implement that in future. Unfortunately, I don't think Hugo has sub-taxonomies. Also, each `booksofbible` term now is a weighted page.

[^1]: Example (fixed)

Light to dark mode logo swap from <https://push.blue/posts/20220718-add-lightdarklogoswap/>

```text
themes\PaperMod\layouts\partials\footer.html
themes\PaperMod\layouts\partials\header.html
```

to

```text
layouts\partials\footer.html
layouts\partials\header.html
```

and then

```html
--- themes\PaperMod\layouts\partials\footer.html        2022-07-18 09:47:47.635823100 -0700
+++ layouts\partials\footer.html                        2022-07-15 13:59:02.482056200 -0700
@@ -75,9 +75,11 @@
         if (document.body.className.includes("dark")) {
             document.body.classList.remove('dark');
             localStorage.setItem("pref-theme", 'light');
+            document.getElementById("siteLogo").src = "/images/pushblue-dark.png";
         } else {
             document.body.classList.add('dark');
             localStorage.setItem("pref-theme", 'dark');
+            document.getElementById("siteLogo").src = "/images/pushblue-light.png";
         }
     })
```

and

```html
--- themes\PaperMod\layouts\partials\header.html        2022-07-18 09:47:47.635823100 -0700
+++ layouts\partials\header.html                        2022-07-15 13:59:02.482056200 -0700
@@ -63,13 +63,35 @@
                     <img src="{{ $img.Permalink }}" alt="logo" aria-label="logo"
                         height="{{- site.Params.label.iconHeight | default "30" -}}">
                 {{- else }}
-                <img src="{{- site.Params.label.icon | absURL -}}" alt="logo" aria-label="logo"
+                <img id="siteLogo" src="{{- site.Params.label.icon | absURL -}}" alt="logo" aria-label="logo"
                     height="{{- site.Params.label.iconHeight | default "30" -}}">
+                    <script>
+                        if (document.body.className.includes("dark")) {
+                            document.getElementById("siteLogo").src = "/images/pushblue-light.png";
+                        }
+                    </script>
                 {{- end -}}
                 {{- end -}}
```

does the trick

And while we're at it, push blue brings up a good point in that the nav seems backwards. this[^reverse] makes it so that the right arrow goes to the future and the left arrow goes to the past.

```html
--- themes\PaperMod\layouts\partials\post_nav_links.html        2022-07-18 09:47:47.635823100 -0700
+++ layouts\partials\post_nav_links.html                        2022-07-18 09:56:20.596032400 -0700
@@ -1,14 +1,14 @@
 {{- $pages := where site.RegularPages "Type" "in" site.Params.mainSections }}
 {{- if and (gt (len $pages) 1) (in $pages . ) }}
 <nav class="paginav">
-  {{- with $pages.Next . }}
+  {{- with $pages.Prev . }}
   <a class="prev" href="{{ .Permalink }}">
     <span class="title">A« {{ i18n "prev_page" }}</span>
     <br>
     <span>{{- .Name -}}</span>
   </a>
   {{- end }}
-  {{- with $pages.Prev . }}
+  {{- with $pages.Next . }}
   <a class="next" href="{{ .Permalink }}">
     <span class="title">{{ i18n "next_page" }} A»</span>
     <br>
```
### 2023.10.03

Trying to get the site back up and I seem to have hit a road block where the page just doesn't have any sort of styling occuring. Above, I discussed that when this happened last (I assume this is for the same issue), I...

> Had to do this too
> <https://stackoverflow.com/questions/65040931/hugo-failed-to-find-a-valid-digest-in-the-integrity-attribute-for-resource>

Now, I think I will use the `head.html` file from the newest version of Papermod with the following code in my `config.yaml` file:

```xml
params:
    assets:
        disableFingerprinting: true
```

[^reverse]: https://push.blue/posts/20220718-reverse-papermodnavlinks/
