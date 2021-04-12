---
title: 'Getting started'
weight: 1
---

Onepage-doc is a open source single page hugo theme for documentation. 

#### Step 1: Install hugo

First you have to install hugo. Follow the [instructions](https://gohugo.io/getting-started/installing) for your os.

#### Step 2: Create a new site

```bash
hugo new site quickstart
```

The above will create a new Hugo site in a folder named quickstart.

#### Step 3: Add the theme

If you are using git, it is recommended to add the theme as a git submodule

```bash
cd quickstart
git init
git submodule add https://github.com/mdjwel/onepage-doc.git themes/onepage-doc
```

If you are not using git, you can:

1. Download the theme as a zip file from [here]()
2. Unzip it in the `themes` directory
3. Rename the folder to `onepage-doc`


Now add the theme to the site configuration

```bash
echo theme = \"onepage-doc\" >> config.toml
```
