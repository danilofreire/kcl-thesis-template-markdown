# Markdown Template for King's College London PhD Thesis

This repository contains a [Markdown](http://en.wikipedia.org/wiki/Markdown) template that conforms to [King's College London's](http://kcl.ac.uk/) [PhD guidelines](http://www.kcl.ac.uk/sspp/departments/politicaleconomy/For-Current-Students/PhD-Handbook-2014-15.pdf). It's a very slightly modified version of [Tom Pollard's](http://tomp.io/) [template](https://github.com/tompollard/phd_thesis_markdown). I'd like to thank him for sharing his work. 

## Why Markdown?

Markdown is a powerful text formatting syntax. It has many benefits:

* **It's fully portable**. You and your friends can edit a Markdown file on any text application on any operating system. No more compatibility errors.
* **It's easy to use**. It looks like text, not like code. The syntax is very simple and can be learnt in a single day. If you can write an email, you can use Markdown.
* **It's worry-free**. You focus on your text and Markdown takes care of the formatting by itself. 
* **It's easy to track changes**. Markdown is pure text, so it works nicely with version control software such as Git or Subversion.
* **It's very flexible**. You can convert a Markdown document to DOC, PDF, HTML, LaTeX, ePub, among other formats. All that with a single line of code.

## Examples

As [John Grueber says](http://daringfireball.net/projects/markdown/), the best way to learn Markdown's syntax is simply to look at a Markdown-formatted document. This is how Markdown handles headers:

````
# Header 1
## Header 2
### Header 3
#### Header 4
````
# Header 1
## Header 2
### Header 3
#### Header 4

Emphasis:

````
*This is italic*. **This is bold**. 
````
*This is italic*. **This is bold**. 

Lists:

````
1. This 
2. is
3. a
4. list

* Unordered
* list
````
1. This 
2. is
3. a
4. list

* Unordered
* list

Links:

````
Welcome to [King's College London](http://kcl.ac.uk/).
````

Welcome to [King's College London](http://kcl.ac.uk/).

Tables:

````
| A            | New              | Table           |
|:-------------|:----------------:|----------------:|
|*left-aligned*|~~centre-aligned~~|**right-aligned**|
|$123          |$456              |$789             |

````

| A            | New              | Table           |
|:-------------|:----------------:|----------------:|
|*left-aligned*|~~centre-aligned~~|**right-aligned**|
|$123          |$456              |$789             |

Easy, isn't it? Please visit [John Grueber's page](http://daringfireball.net/projects/markdown/) to know more about Markdown. [This tutorial](http://markdowntutorial.com/) is a good place to learn the basics of the language and [this cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) is a great reference.

## Why should I *not* use Markdown?

Tom ranks some reasons why Markdown is not (yet) perfect:

> There are some minor annoyances:
- if you haven't worked with Markdown before then you'll find yourself referring to the style-guide fairly often at first.
- it isn't possible to add a short caption to figures and tables. This means that /listoftables and /listoffigures include the long-caption, which probably isn't what you want. If you want to include the list of tables and list of figures, then you have to write them manually.
- all of the style documents in this framework could be improved. The PDF output is acceptable as it is, but HTML and Word need work if you plan to use these formats.

But they're indeed minor annoyances. The pros surely outweigh the cons :)

## What do I need to write my thesis using this template?

First, fork or [download](https://github.com/danilofreire/kcl-thesis-template-markdown/archive/master.zip) this repository.

Then, install a simple text editor. It's very likely that you already have one. Anything that can edit a `.txt` file will do the job ([Notepad](http://en.wikipedia.org/wiki/Notepad_%28software%29), [gedit](http://en.wikipedia.org/wiki/Gedit), etc). You can also use an [online](https://stackedit.io/) [editor](http://dillinger.io/) if you prefer. Edit the files in the source directory, save them as `.md` and you're already writing your thesis. Mathematical formulas can be typed using LaTeX code, e.g., `$ y = \beta_{0} + \beta_{1} x + \epsilon $`

Add your references to `references.bib`. If you're using Google Scholar, click on "Cite" below the article link and choose "Import into BibTeX". An example: suppose you want to cite John Nash's "Non-cooperative games" article. If you search for the paper on [Google Scholar](http://scholar.google.co.uk/scholar?hl=en&q=john+nash+non-cooperative&btnG=&as_sdt=1%2C5&as_sdtp=) you will see something like this:

````
@article{nash1951non,
  title={Non-cooperative games},
  author={Nash, John},
  journal={Annals of mathematics},
  pages={286--295},
  year={1951},
  publisher={JSTOR}
}
````

Just copy and paste the text onto the `.bib` file and you're done. To cite Nash's paper in your thesis, just type `[@nash1951non]`. More about citations [here](http://stackoverflow.com/questions/13607156/autocomplete-pandoc-style-citations-from-a-bibtex-file-in-emacs).  

Finally, you'll need [LaTeX](http://latex-project.org/ftp.html) and [Pandoc](http://johnmacfarlane.net/pandoc/README.html) to convert your Markdown output to pdf. Go to the folder that contains "Makefile" and type `make pdf` at your command line. Your pdf will be on the "output" folder.

Some important reminders from Tom:

> - each chapter must finish with at least one blank line, otherwise the header of the following chapter may not be picked up.
- add two spaces at the end of a line to force a line break.
- the template uses [John Macfarlane's Pandoc](http://johnmacfarlane.net/pandoc/README.html) to generate the output documents. Refer to this page for Markdown formatting guidelines.
- PDFs are generated using the Latex templates in the style directory. Fonts etc can be changed in the tex templates.
- To change the citation style, just overwrite ref_format.csl with the new style. Style files can be obtained from [citationstyles.org/](http://citationstyles.org/)

## Changes to the original template

I've added some minor changes to the original repository:

* References are formatted in [Chicago style](https://owl.english.purdue.edu/owl/resource/717/01/). 
* King's logo was added to the title page
* Fonts were changed to [Libertine](http://en.wikipedia.org/wiki/Linux_Libertine) because the previous one didn't work well on Ubuntu Linux (14.04 LTS)
* Added Libertine to figure and table captions
* Increased or reduced vertical space throughout the file
* Added a different text for the statement of academic integrity

All changes can be easily reverted if necessary. For instance, if you want to use the default [Computer Modern](http://en.wikipedia.org/wiki/Computer_Modern) font instead of Libertine, just add `%` before `\usepackage[osf]{libertine}` in `preamble.tex`.

## Comments and suggestions

Feel free to send me a message if you find any mistake or have any suggestion to improve this repository. Once again, thanks to Tom Pollard for providing his template. I hope this repository is useful and I wish you a good time at King's :)
