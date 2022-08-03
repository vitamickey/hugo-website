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
# description: "Desc Text."
# canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
# ShowReadingTime: true
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
title: "VSCode"
date: 2022-05-26T09:26:13+10:00
tags: ["vscode", "technology"]
lastmod: 2022-07-30
---

I think you call this a stack, where you talk about applications you use and their setup. So, I am gonna write a university stack, or a general productivity stack, but this is my VSCode stack, which in essence is a list of extensions I use and my setup.

- **Colour Theme:** [Rouge](https://marketplace.visualstudio.com/items?itemName=josef.rouge-theme)
  - I like navy and the soft pink is really nice.
    -I also have used *Horizon Bright* by jolaleye if I ever want to use a light theme (so, not super often, but enough to say I like it as a theme). This isn't available on VSCode marketplace anymore, but other versions have been made of it.
  - I am trying out [Natural](https://marketplace.visualstudio.com/items?itemName=naturalTheme.natural-theme) by Marco Franzese
  - Name: [Paddy Color Theme](https://marketplace.visualstudio.com/items?itemName=yile-ou.paddy-color-theme) has a really nice variety of colour themes too, which I use occasionally.
- **Font:** Fira Mono
- **File Icon Theme:** [Field Lights Theme](https://marketplace.visualstudio.com/items?itemName=sveggiani.vscode-field-lights)
- **LaTeX:**
  - see below
- **Markdown:**
  - [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
  - [Markdown+Math](https://marketplace.visualstudio.com/items?itemName=goessner.mdmath)
  - [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
    - `<!-- markdownlint-disable MD033 -->` is very nice for ignoring HTML in markdown
- **Hugo:**
  - [Hugo Language and Syntax Support](https://marketplace.visualstudio.com/items?itemName=budparr.language-hugo-vscode)
- **R:**
  - see below
- **GitHub:**
  - [GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) so far I have used it and it's been a game-changer but people seem to really dislike it on the marketplace reviews lol
- **Other**
  - I have some **Jupyter** extensions installed but I don't really use Jupyter that much. I needed it for one statistics class iirc, but for statistics I prefer to use R separately to VSCode (at most, I will edit code in VSCode).
  - I have [Music Time for Spotify](https://marketplace.visualstudio.com/items?itemName=softwaredotcom.music-time) installed, but I don't really use it.
  - I have all the basic **Python** extensions installed but, again, only needed for one class. I don't use Python much now, and I am quite bad at it anyway lol.
  - I recently downloaded the **Go** extension since I need to use it to download `hugo-extended`, but like, I don't think I need the extension.
  - ~~Oh, and I use **GitHub**, but you don't need extensions for that haha.~~

## Using R in VSCode

WOW I just set up R properly to see if I could break free from RStudio and thank goodness it seems to have worked. Prerequisites to follow the instructions are that you need GitHub, R (and rtools package), and Python (and pip).

- Following
  - R in Visual Studio Code from the official VSCode docs at <https://code.visualstudio.com/docs/languages/r#_getting-started>
  - Installation docs from REditorSupport at <https://github.com/REditorSupport/vscode-R/wiki/Installation:-Windows> because for some reason the official VSCode docs don't include downloading the debugger
- I didn't know what `r.rterm.windows` meant lol
  - "The quite mysterious instructions refer simply to the setting in the R extension in Visual Studio Code. To set this value to the R executable path, these are the steps in VS Code 1.35.1 on Windows. `File > Preferences > Extensions`. Right click on the R extension and Configure Extension Settings. In the R > Rterm: Windows cell, paste the path to the R executable."[^1]
- You end up installing
  - [R](https://cloud.r-project.org/)
  - `languageserver` in R ([link](https://github.com/REditorSupport/languageserver))
    - from CRAN (i.e. in the R terminal) with `install.packages("languageserver")`
  - [R for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=REditorSupport.r)
  - [radian](https://github.com/randy3k/radian), a modern R console
    - requires Python and pip
    - change extension settings: `"r.bracketedPaste": true` and `"r.rterm.windows":"C:\\Users\\user\\AppData\\Local\\Programs\\Python\\Python37\\Scripts\\radian.exe"`
      - can just search "bracketed paste" and "rterm windows" in settings, or change JSON I think
  - [httpgd](https://github.com/nx10/httpgd)
    - from CRAN with `install.packages("httpgd")`
    - change extension settings: enable `r.plot.useHttpgd` to true
      - can just search "useHttpgd" in settings
  - [R Debugger](https://marketplace.visualstudio.com/items?itemName=RDebugger.r-debugger)
    - needs [vscDebugger](https://github.com/ManuelHentschel/vscDebugger)
      - I installed with `remotes::install_github("ManuelHentschel/vscDebugger")`
        - requires GitHub I think but more importantly [Rtools](https://cran.r-project.org/bin/windows/Rtools/) which is surprisingly large
- I could install
  - `rmarkdown` with `install.packages("rmarkdown")`
    - I don't use R markdown tho so

bada bing bada boom [R](/r/) now works on my VSCode. this took too long.

## Using LaTeX in VSCode

*SETTING UP VISUAL STUDIO CODE FOR LATEX* by Peter W. Smith shows how to set up LaTeX with a linguistics focus, which is coincidentally convenient for me: <https://pwsmith.github.io/2020/06/05/setting-up-a-text-editor-for-latex-vscode/>. Another setup, *How to set up VS Code for LaTeX* by Marlene Mayr: <https://marlenemayr.github.io/blog/latex-in-vscode>.

- [*LaTeX Workshop* by James Yu](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) for ease of LaTeX editing, building, viewing outputs, etc., really all you nee for it to run
- [*LaTeX language support* by Long Nhat Nguyen](https://marketplace.visualstudio.com/items?itemName=torn4dom4n.latex-support) for syntax highlighting and such.
- [*LaTeX* by Mathematic](https://marketplace.visualstudio.com/items?itemName=mathematic.vscode-latex) which acts as a linter for LaTeX with the `chktex` package
- [*Insert Unicode*](https://marketplace.visualstudio.com/items?itemName=brunnerh.insert-unicode) for unicode lol

## Other things

Set tab size per file type. Markdown causing me pain with it's tab size of 2... but it's fixed now. <https://stackoverflow.com/questions/34247939/how-to-set-per-filetype-tab-size>

On that note, this is a more comprehensive stack post about tab size, indents as spaces and inherit <https://stackoverflow.com/questions/36814642/visual-studio-code-convert-spaces-to-tabs#:~:text=There%20are%203%20options%20in.vscode%2Fsettings.json%3A%20%2F%2F%20The%20number,detected%20based%20on%20the%20file%20contents.%20%22editor.detectIndentation%22%3A%20true>

Snippets: for dashes, <https://fotoallerlei.com/blog/post/2020/typing-en-and-em-dashes-in-vs-code/post/>

[^1]: https://superuser.com/questions/1455225/how-to-install-r-extension-in-visual-studio-code#:~:text=File%20%3E%20Preferences%20%3E%20Extensions%20Right%20click%20on,cell%2C%20paste%20the%20path%20to%20the%20R%20executable
