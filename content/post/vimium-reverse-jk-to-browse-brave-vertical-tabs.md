---
title: 'Vimium - Reverse J/K to Browse Brave Vertical Tabs'
date: 2024-04-28T11:11:38+02:00
# weight: 1
# aliases: ["/first"]
tags: ['vimium', 'brave browser']
categories: ['tech', 'tutorials']
author: 'Phuc Tran' # multiple authors: ["Me", "You"]
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
description: 'How to reverse J/K in Vimium to browse Brave vertical tabs.'
summary: 'How to reverse J/K in Vimium to browse Brave vertical tabs.'
canonicalURL: "https://glup3.dev/post/vimium-reverse-jk-to-browse-brave-vertical-tabs/"
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
# cover:
#   image: '<image path/url>' # image path/url
#   alt: '<alt text>' # alt text
#   caption: '<text>' # display caption under cover
#   relative: false # when using page bundles set this to true
#   hidden: true # only hide on current single page
# editPost:
#     URL: "https://github.com/glup3/blog-v2/{content}"
#     Text: "Suggest Changes" # edit text
#     appendFilePath: true # to append file path to Edit link
---

## Situation

I am using Brave's vertical tabs and Vimium. The default keybindings for browsing between tabs is `SHIFT + J/K` for `previous` and `next` tab, but when I press `J` I want to navigate to the next tab instead of the previous one.

## Solution

The solution is to remap the keybindings in the Vimium options.

```vimrc
map K previousTab
map J nextTab
```

## Acknowledgement

Thanks to Stephen Blott for sharing his solution back in 2018.

https://github.com/philc/vimium/issues/2948#issuecomment-364017167
