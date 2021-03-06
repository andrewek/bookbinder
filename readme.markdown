# Bookbinder

Goal: Given structured markdown, output a beautiful-ish PDF with a simple bash
script. We want to package this script in some shareable way so that it can be
simply included in relevant projects (and possibly invoked by a CI/CD pipeline?)

We want to be able to:

+ Write in markdown
+ Render highlighted code in a variety of languages
+ Have a dynamically-created table of contents
+ Page numbers, etc.
+ Properly resize and compress images
+ Be able to render diagrams like what you might create with GraphViz, etc.
+ Use some sort of theming on the output

Ideally, we can define steps, choose options, define dependencies, and set
variables with a JSON file or something like that.

Our pipeline will probably be:

1. Markdown -> base content
2. pp -> insert cool stuff
3. Pandoc -> convert to LaTeX
4. ??? -> PDF/epub/mobi export

Sources:

+ https://pianomanfrazier.com/post/write-a-book-with-markdown/
+ http://cdsoft.fr/pp/
+ https://pianomanfrazier.com/post/write-a-book-with-markdown/
+ https://www.latextemplates.com/cat/books
  + https://github.com/Wandmalfarbe/pandoc-latex-template
