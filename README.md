# 18F/slides

```
   #    #####               #                                      
  ##   #     # ######      #   ####  #      # #####  ######  ####  
 # #   #     # #          #   #      #      # #    # #      #      
   #    #####  #####     #     ####  #      # #    # #####   ####  
   #   #     # #        #          # #      # #    # #           # 
   #   #     # #       #      #    # #      # #    # #      #    # 
 #####  #####  #      #        ####  ###### # #####  ######  ####  
                                                                   
```
# Why 18F/slides

You should use 18F/slides if you:

1. Can do Markdown,
2. Want a stupidly simple way to hack up a presentation,
3. Want a URL for your slide deck, and
4. Want `git`.

# How to Use 18F/slides

To use 18F/slides:

1. Create a new markdown file in the `_slides` directory.
2. Add yaml frontmatter to the file with the following:

	```
	---
	layout: default
	path: path-to-url
	title: Title for 18F/slides
	---
	```

3. Create slides, using markdown syntax (technically, it's kramdown, go nuts).
4. Separate slides using `---` for horizontal pagination between slides and `--` for vertical pagination.
5. Commit the file to the `gh-pages` branch of the 18F/slides repo.
6. Profit. See example [here](http://18f.github.io/slides/sample/#/).

# How does it work?

18F/slides leverages the amazing open-source [reveal.js](https://github.com/hakimel/reveal.js/) library and [jekyll](http://jekyllrb.com) and is hosted on [github pages](https://pages.github.com/).

# How can I make it better?

See [CONTRIBUTING.md](https://github.com/18F/slides/blob/gh-pages/CONTRIBUTING.md).

# Forking
If you'd like to use Slides for your own organization, here are some tips on how to fork it and get your own version:

1. Fork! (duh)
2. Edit _config.yml. Modify title/email and - critically - the "url" field to reflect your github account.
3. Wait for a little while - Github Pages is working behind the scenes for your initial setup,  and if you try to actually view your slides right away, you'll probably get a 404. It sometimes takes 5-10 minutes; once it's set up initially, changes take effect pretty quickly.
3. Drop in your own logo file to replace the current one - assets/css/theme/images/logo.svg (or edit the current theme to reflect your logo URL or go without a logo, see below)
4. You'll probably want to define your own theme at some point (your CSS goes ../assets/css/theme), and edit _layouts/default.html to reflect it. Look for the link with id="theme" in it.
5. That's it! Enjoy your slides.
