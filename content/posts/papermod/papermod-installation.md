---
title: "Installation | Update"
summary: Read Install and Update instructions here
date: 2020-09-15T11:30:03+05:30
series: ["PaperMod"]
weight: 1
aliases: ["/papermod-installation"]
tags: ["PaperMod"]
author: "Aditya Telange"
showToc: true
TocOpen: true
---

## Guide

Follow [Quick Start](https://gohugo.io/getting-started/quick-start/) guide to setup hugo and create a new site.
Make sure you install latest version of **`hugo(>=0.74.0)`**.

After you have created a new site, at [Step 3](https://gohugo.io/getting-started/quick-start/#step-3-add-a-theme) follow the steps:

### Method 1

Inside the folder of your Hugo site, run:

```bash
git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
```

**Note**: You may use ` --branch v3.0` to end of above command if you want to stick to specific release.

> Updating theme :
>
> ```bash
> cd themes/PaperMod
> git pull
> ```

### Method 2

you can use as [submodule](https://www.atlassian.com/git/tutorials/git-submodule) with

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod --depth=1
git submodule update --init --recursive
```

**Note**: You may use ` --branch v3.0` to end of above command if you want to stick to specific release.

> Updating theme :
>
> ```bash
> git submodule update --remote --merge
> ```

### Method 3

Or you can Download as Zip from Github Page and extract in your themes directory

### Finally ...

Add in `config.yml`:

```yml
theme: "PaperMod"
```

---

## Quick Links

-   ### [Papermod - Features](../papermod-features)

-   ### [Papermod - How to Guide](../papermod-how-to)

-   ### [Papermod - Icons](../papermod-icons)

-   ### [ChangeLog](https://github.com/adityatelange/hugo-PaperMod/releases)

---

## Sample `config.yml`

> **Example Site Structure is present here**: [exampleSite](https://github.com/adityatelange/hugo-PaperMod/tree/exampleSite/)

**Use appropriately**

```yml
baseURL: "https://examplesite.com"
title: ExampleSite
paginate: 5
theme: hugo-PaperMod

enableRobotsTXT: true
buildDrafts: false
buildFuture: false
buildExpired: false

googleAnalytics: UA-123-45

minify:
    disableXML: true
    minifyOutput: true

params:
    env: production # to enable google analytics, opengraph, twitter-cards and schema.
    title: ExampleSite
    description: "ExampleSite description"
    author: Me
    # author: ["Me", "You"] # multiple authors

    images: ["<link or path of image for opengraph, twitter-cards>"]

    ShowReadingTime: true
    ShowShareButtons: true
    comments: false
    defaultTheme: auto
    disableThemeToggle: false
    disableSpecial1stPost: false

    assets:
        # disableHLJS: true # to disable highlightjs
        # disableFingerprinting: true
        favicon: "<link / abs url>"
        favicon16x16: "<link / abs url>"
        favicon32x32: "<link / abs url>"
        apple_touch_icon: "<link / abs url>"
        safari_pinned_tab: "<link / abs url>"

    label:
        text: "Home"
        icon: /apple-touch-icon.png
        iconHeight: 35

    # profile-mode
    profileMode:
        enabled: false # needs to be explicitly set
        title: ExampleSite
        imageUrl: "<img location>"
        imageWidth: 120
        imageHeight: 120
        imageTitle: my image
        buttons:
            - name: Posts
              url: posts
            - name: Tags
              url: tags

    # home-info mode
    homeInfoParams:
        Title: "Hi there \U0001F44B"
        Content: Welcome to my blog

    socialIcons:
        - name: twitter
          url: "https://twitter.com/"
        - name: stackoverflow
          url: "https://stackoverflow.com"
        - name: github
          url: "https://github.com/"

    analytics:
        google:
            SiteVerificationTag: "XYZabc"

    cover:
        hidden: true # hide everywhere but not in structured data
        hiddenInList: true # hide on list pages and home
        hiddenInSingle: true # hide on single page

    # for search
    # https://fusejs.io/api/options.html
    fuseOpts:
        isCaseSensitive: false
        shouldSort: true
        location: 0
        distance: 1000
        threshold: 0.4
        minMatchCharLength: 0
        keys: ["title", "permalink", "summary", "content"]
menu:
    main:
        - identifier: categories
          name: categories
          url: /categories/
          weight: 10
        - identifier: tags
          name: tags
          url: /tags/
          weight: 20
        - identifier: example
          name: example.org
          url: https://example.org
          weight: 30
```

---

## Sample `Page.md`

```yml
---
title: "My 1st post"
date: 2020-09-15T11:30:03+00:00
weight: 1
aliases: ["/first"]
tags: ["first"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
disableShare: false
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
comments: false
description: "Desc Text."
disableHLJS: true # to disable highlightjs
---

```

---
