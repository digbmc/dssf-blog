# [DSSF 2022 Blog Site](https://cboucher01.github.io/dssf-blog/)

## Site function

The Digital Scholarship Summer Fellow Blog was a beginner project for the fellows to develop our web-development skills while creating a site to host our blog posts and information about us and the digital web design toolkit that we are currently building. During the coding process, we came across multiple challenges, including aligning our navbar, coordinating work on the site with multiple people using GitHub, organizing our workflow requests, and finally, deploying the site on GitHub. In the future, we are considering adding onto the site to make it a library depot for our learning resources for our future project, the digital web design toolkit. 

### Which kinds of code did we use?
- HTML
- SCSS
- JavaScript/Bootstrap
- Jekyll/Ruby

## Working with Minima
This site was created by editing Minima, Jekyll's first and default theme. As the default theme, Minima was a useful resource for developing the DSSF 2022 blog.

Though there were various aesthetic changes made to the layout, navigation bar, background, post box, titles, headers, and more, portions of our site still rely on Minima to operate.

You can compare our code and find out more about Minima [here](https://github.com/jekyll/minima).

## How-to install and run
The best way to run this project is to click on the website link [here](https://cboucher01.github.io/dssf-blog/).

If you would like to make changes or add edits to the code, you can do that by forking this repository and adding it to your personal repositories on GitHub. From there, you can make changes directly on GitHub or download onto your computer and open with the VS Code application or your preferred text editor. 

## How to make a site like this one
- Adding collections (like fellows)
- Changing SCSS files to change the look of the site
- Creating our own skin based on the skins that come with Minima
- The creature background (what we did and how you might do it better with vectors instead of raster images)

### Navbar
- To view the code used for the navigation bar: locate the folder labeled "_ includes" then open the file labeled "header.html". Code for the navigation bar begins at <nav class=...
- This navigation bar was created by following the Bootstrap 4.0 Documentation found [here](https://getbootstrap.com/docs/4.0/components/navbar/). While Minima has responsive elements within the theme, for the sake of our project goals this summer we wanted to learn more about Bootstrap by integrating this navigation bar ourselves.
- Within the folder labeled "_sass\minima" in the file "_layout.scss" we adjusted the padding and alignment of the navigation bar under the "site.nav" section and added further styling.
```
  .site-nav {
    position: absolute;
    top: $spacing-unit / 2;
    right: $spacing-unit / 2;
    background-color: $background-color-2;
    border: 1px solid $border-color-01;
    padding: 10px;
    border-radius: 5px;
    text-align: right;
    flex-wrap: nowrap;
  
    }
```
- You can load the Minima sample site to view the differences between the default navigation bar and ours in appearance, or open the page source (right click on the page and select view page source from the dropdown) to compare the code in your browser.
- If you are building the Bootstrap 4.0 Navbar into your Jekyll site through the default Minima theme like we did and notice an alignment error when minimizing the desktop window (or on mobile) where the opened menu is not inline with the Site Title, we fixed this problem by adding "flex-wrap: nowrap;" to the "_layout.scss" file under the "site.nav" section. 

### Customizing templates: creating our lemon-lime theme
In order to change the color palette and overall theme of the website, we used a feature called “skins.” Skins allow you to create an entire theme that, with just editing a line of code, you can change your website's fonts, font colors, background, opacity, and really anything else you'd like. If you  

According to [Minima](https://github.com/jekyll/minima), you should start out with *at least* the following code in your `assets/css/style.scss` file
```
---
---

@import "minima/skins/{{ site.minima.skin | default: 'classic' }}";
@import "minima/initialize";
```

To design our signature “lemon-lime” theme used on our site, we copied the code of the classic minima skin, copied it all into a new file called `lemon-lime.scss` , and then changed code and added new code, like `$background-color-1:      #82a573 !default;` to create the new skin. 
```
.
├── _sass/minima
└── skins
    └── lemon-lime.scss
```

Then, in order to view our changes on our website, we updated the `assets/css/style.scss` file to include the default theme 'lemon-lime' instead of 'classic,' which updated our changes. 

## Useful resources:
- [Minima](https://github.com/jekyll/minima)
- [Jekyll Docs](https://jekyllrb.com/docs/)
- [Liquid Docs](https://shopify.github.io/liquid/)
