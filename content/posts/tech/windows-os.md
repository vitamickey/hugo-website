---
date: 2022-09-21
title: "Windows OS"
tags: ["technology"]
alises: ["Windows"]
lastmod: 2022-09-21
---

Whilst trying to list out my files in my movie drive

<https://www.minitool.com/news/how-to-open-drive-in-cmd.html>

To open `D:/>`, type command

```cmd
D:
```

<https://www.get-itsolutions.com/how-to-list-files-in-cmd-command-prompt-windows-10/#:~:text=How%20to%20create%20a%20text%20file%20listing%20of,as%20the%20main%20folder%2C%20enter%20the%20following%20command>

To list folders, open directory in command line and type

```cmd
dir > listoffiles.txt
```

or for *subfolders* included

```cmd
dir /s >listoffiles.txt
```

or give *full path name*

```cmd
dir >D:\listmyfiles.txt
```

or give list of *only a certain file type*, like PDFs

```cmd
dir /s *.pdf >listpdf.txt
```
