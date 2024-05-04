---
title: "How to Select Random Option with Playwright"
date: 2024-05-04T16:30:29+02:00
tags: ['playwright', 'browser automation']
categories: ["tech", "tutorials", "til"]
author: "Phuc Tran" # multiple authors: ["Me", "You"]
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Short snippet on how to select a random <option> with Playwright."
canonicalURL: "https://glup3.dev/post/playwright-how-to-select-random-option"
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
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---

## Situation

My task was to create random test data for an application, which didn't have an API for data creation. I simply chose to write e2e tests with Playwright and I only had to figure out how to select random values.

## Solution

After googling, looking on Stackoverflow and asking ChatGPT - I managed to write the following code.

```typescript
import { test } from '@playwright/test'

test('select random option', async ({ page }) => {
    // you can also use any other locator
    const select = page.locator('#id_of_the_select')
    const options = select.locator('option')

    // sometimes you want to exclude the first option, change it to 1
    const min = 0
    const max = (await options.count()) - 1
    const index = Math.floor(min + Math.random() * (max - min + 1))

    await select.selectOption({ index: index })
})
```
