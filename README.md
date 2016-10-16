# BFUI_Hugo

![BFUI](https://github.com/lasseborly/BFUI_Hugo/blob/master/images/screenshot.png "BFUI")

A jab at recreating the menu UI of Battlefield in the browser and with Hugo

This is a fan project that tries to recreate the Battlefield 1 UI with web technologies.
The main menu UI elements are more or less exact derivatives from the games menu but some of the residing UI elements has been imagined in the vision of Battlefield 1's design.
The design is made to be responsive and work across desktop, tablet, and mobile as well.

This is the Hugo theme implementation of the theme.

## Features
* __Static pages__ - Create static pages and access them via the menu.
* __Blog__ - Make blog posts in best Battlefield fashion.
* __Menu__ - Reference your static pages and your blog from the menu.

## Getting Started
From the root of you Hugo site clone the theme into `themes/BFUI_Hugo` by running:

```
  git clone https://github.com/lasseborly/BFUI_Hugo.git themes/BFUI_Hugo
```

## Usage
To use BFUI_Hugo you must first, from the root of your Hugo site, run either:

```
  hugo -t BFUI_Hugo
```

or set in you `config.toml`.

```
  theme = "BFUI_Hugo"
```

## Configuration
You can set the normal Hugo site variables in your `config.toml` but there is also some custom BFUI_Hugo variables you can set. This is an example of a full `config.toml`.

```toml
theme = "BFUI_Hugo"
baseurl = "https://hugosite.com"
languageCode = "en-us"
title = "BFUI"

[params]
  description = "A jab at making the BFUI in HTML/CSS"
  author = "Anders Enghøj & Lasse Borly"
	subtitle = "Battlefield UI"

  heroTitle = "Welcome to BFUI - Good luck soldier!"
  heroContent = "A UI framework inspired by the Battlefield games"
  heroImage = "bg3.jpg"

[menu]
  [[menu.main]]
      name = "Home"
      weight = 1
      identifier = "home"
      url = "/"

  [[menu.main]]
      name = "Posts"
      weight = 2
      identifier = "posts"
      url = "/post/"

  [[menu.secondary]]
      name = "Power"
      weight = 1
      identifier = "power"
      url = "/power"
```

If you want your static content pages represented in the menu you have to add menu info like so:

```markdown
+++
date = "2011-03-18"
title = "About"
id = "about"
[menu]
  [menu.main]
    name = "About"
    weight = 3
+++
```

## Contributing

1. Fork it
2. Create your feature branch
```
  git checkout -b my-new-feature-or-fix
```
3. Commit your changes
```
  git commit -am 'Add some feature-or-fix'
```
4. Push to the branch
```
  git push origin my-new-feature-or-fix
```
5. Create new Pull Request

## Extra
Take a look at my [docker setup](https://github.com/lasseborly/hugo-development) for developing with Hugo. It's, again, very simple, straight forward and open for contributions.
