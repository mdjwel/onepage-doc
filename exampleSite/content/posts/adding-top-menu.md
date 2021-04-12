---
title: Adding a top menu
wight: 4
---

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
