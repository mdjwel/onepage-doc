## Getting started
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


## Add a section

Now you can start adding sections to you documentation. Add a file in the `content/posts ` directory with an `.md` extension. Add a frontmatter like this at the beginning: 

```markdown
---
title: 'Add a section'
weight: 0
---
```
The weight is used for ordering of the sections. Post with higher weights will appear fist.

In the rest of the file you can use markdown to write your content.

## Changing the logo
Put your logo in the `static` directory and add it in the config

```toml
[params]
logo = '<you file name>'
logo2x = '<your file name>'
```

You can actually add four versions of the logo:
* `logo`
* `logo2x` a high resolution version of the logo
* `logo-w` logo for dark mode
* `logo-w2x` high resolution logo for dark mode

## Adding a top menu

You can add a menu in the top by adding the entries in the config:

```toml
[menu]
[[menu.main]]
name = 'Menu item 1'
url = '<link for item 1>'

[[menu.main]]
name = 'Menu item 2'
url = '<link for item 2>'
```

You can also assign weights to the items to sort them.

The menu can be nested by assigning parent to the items:

```toml
[menu]
[[menu.main]]
name = 'Parent item'
identifer = 'parent'

[[menu.main]]
name = 'Menu item 1'
url = '<link for item 1>'
parent = 'parent'

[[menu.main]]
name = 'Menu item 2'
url = '<link for item 2>'
parent = 'parent'
```
