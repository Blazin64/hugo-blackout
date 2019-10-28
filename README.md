# Blackout

Are all those light Hugo themes out there burning your eyes? Well, Blackout may be the solution for your problem!

This theme was created with a focus on minimalism, both in terms of code and visual appearance. No 2000-line CSS files here!

Never heard of Hugo? It's the best static site generator, hands down! Check it out at [gohugo.io](https://gohugo.io/)!

Screenshots will be added once this theme is considered complete.

### Customization

A nice set of color variables is at the top of `static/css/style.css` to make it easy to modify the theme's colors to fit your tastes. The variable names are all fairly self-explanatory.

You will probably want to display a logo and a quick description at the top of the home page. The best way to do this, once you have generated a new site, is to add an `_index.md` file under the `content` directory. Make sure to remember that Hugo assumes all images are in your site's `static` directory. The CSS included with this theme will automatically center the content of your `_index.md` file.
Example `_index.md`:
```
![logo](your-logo-here.png)

Your site description here.
```
