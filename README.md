# Blackout

Are all those light Hugo themes out there burning your eyes? Well, Blackout may be the solution for your problem!

This theme was created with a focus on minimalism, both in terms of code and visual appearance. No 2000-line CSS files here!

Never heard of Hugo? It's the best static site generator, hands down! Check it out at [gohugo.io](https://gohugo.io/)!

![screenshot](https://raw.githubusercontent.com/Blazin64/hugo-blackout/master/images/screenshot.png)

### Getting Started

I recommend taking a look at the [Install Hugo](https://gohugo.io/getting-started/installing) and [Quick Start](https://gohugo.io/getting-started/quick-start) pages if you are new to Hugo. I have provided a quick summary of the required steps for a Linux PC below.

##### Requirements
 * Hugo, see [Install Hugo](https://gohugo.io/getting-started/installing).
 * Git, see [Set up Git](https://help.github.com/en/github/getting-started-with-github/set-up-git) or [Installing Git](https://gist.github.com/derhuerst/1b15ff4652a867391f03).

##### Setup

1. Generate a new site. Open a terminal in a directory of your choice and run:

```
hugo new site YOUR_SITE_NAME
```

  * There will now be a new directory with the name you used. It has the basic structure of a Hugo site inside.

2. Navigate into this new directory, delete the `archetypes` directory, and install the Blackout theme. (Don't worry, the theme already has an archetype file built in.)

```
cd YOUR_SITE_NAME
rm -r archetypes
git init
git submodule add https://github.com/Blazin64/hugo-blackout.git themes/blackout
```

3. Enable the Blackout theme and set Hugo to display 5 items per page.

  * Open your site's configuration file with your favorite text editor (I use the `vi` text editor here, but anything else will work just as well.)

```
vi config.toml
```

  * Add the following:

```
paginate = "5"
theme = "blackout"
```

  * You may want to make further edits to `config.toml`, such as changing the default `title` entry.

4. Create a new post and add some content to it.

```
hugo new posts/example-post.md
vi posts/example-post.md
```

5. Test your new site. (The `-D` option allows draft posts to be shown.)

```
hugo server -D
```

  * Navigate to http://localhost:1313 in your web browser to see it. Kill the Hugo server with <kbd>ctrl</kbd> + <kbd>c</kbd> when you're done.

6. Once everything is to your liking, set `draft: false` at the top of your post file and generate your pages. (I use the `vi` text editor here, but anything else will work just as well.)

```
vi posts/example-post.md
hugo
```

  * Hugo will put your generated pages under the `public` directory.

7. Publish your site. Put the contents of the `public` directory on a server. [GitHub Pages](https://pages.github.com/) is good option, and it's free!

Repeat steps 4-7 whenever you want to add more content.


### Theme Updates

Updating the theme is pretty simple. Open a terminal in your site directory and run:

```
git submodule update --remote themes/blackout
```

### Customization

A nice set of color variables is at the top of `static/css/style.css` to make it easy to modify the theme's colors to fit your tastes. The variable names are all fairly self-explanatory.

You will probably want to display a logo and a quick description at the top of the home page. The best way to do this, once you have generated a new site, is to add an `_index.md` file under its `content` directory. If you use a relative URL (like in the example below) for any images you want to embed, make sure to include a slash at the beginning. Also, remember that Hugo assumes all images are in your site's `static` directory. The CSS styling included with this theme will automatically center the content of your `_index.md` file.

Example `_index.md`:

```
![logo](/your-logo-here.png)

Your site description here.
```
