# Slideshow with MARP on Ryan Hill Studio web project.

A presentation by Nick Golebiewski
Topic: Ryan Hill Studio website design and engineering

Uses MARP. Markdown -> Slideshow -> Actions to publish via Github as website

Thx!

-Nick

https://ryanhill.studio

### CLI commands for making the slideshows (assumed MARP is installed)

Output PDF: ```marp ryanhillstudio_pinterest_presentation.md -o pdf_archive/ryanhill_presentation_v2.pdf --allow-local-files```

Serve HTML Preview: ``` marp ryanhillstudio_pinterest_presentation.md -o index.html --preview```

Make HTML: ```marp ryanhillstudio_pinterest_presentation.md -o test.html --allow-local-files```


### Version Notes

* V1
  * 15 minutes
  * Verbose design decisions for tech stack
  * 3 total full examples for tech challenges
    * Video embedding
    * Image upload issue (unique constraint/stale JSON login tokens)
    * Hydration Issues with JSON Web Token in Nuxt

* v2
  * 10 minutes
  * tech stack to 1 slide
  * 1 challenge (image upoad issue)

* current
  * ? but <10  minutes
  * remove more 'setup' and intentions before web demo
  