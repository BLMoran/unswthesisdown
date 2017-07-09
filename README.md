# unswthesisdown

This is a fork of [ismayc/thesisdown](https://github.com/ismayc/thesisdown) designed to produce theses for UNSW students. Write your thesis in RMarkdown! Installation is mostly as the original `thesisdown` package, described below, but for the modified repo and package name:

```S
install.packages("devtools")
devtools::install_github("rstudio/bookdown")
devtools::install_github("rensa/unswthesisdown")
```

In RStudio (step 3 below), the template will appear as 'UNSW Thesis'. Once you've created a new RMarkdown document in R or RStudio using the blow instructions, all you need to do it replace the .Rmd files with your own. You should also modify the YAML (metadata) at the top of index.Rmd to fill in details like your name and school, as well as some of the preliminary matter. You can also use this to switch between PDF and HTML output.

Note that Word and EPUB output are available, but neither have been modified for UNSW: the Word template is from Reed College (so don't submit it!) and the EPUB is, I think, based on the bookdown default (so not great). Stick to Gitbook while you write and switch to PDF as you get toward submission.

If you have any UNSW-specific feedback, add an issue, send me a PR or [get in touch](twitter.com/rensa_co) :)

# thesisdown

This project was inspired by the [bookdown](http://github.com/rstudio/bookdown) package and is an updated version of my Senior Thesis template in the `reedtemplates` package [here](http://github.com/ismayc/reedtemplates).

Currently, the PDF and gitbook versions are fully-functional.  The word and epub versions are developmental, have no templates behind them, and are essentially calls to the appropriate functions in bookdown.

The current output for the four versions is here:
- [PDF](https://github.com/ismayc/thesisdown_book/blob/gh-pages/thesis.pdf) (Generating LaTeX file is available [here](https://github.com/ismayc/thesisdown_book/blob/gh-pages/thesis.tex) with other files at in the [book directory](https://github.com/ismayc/thesisdown_book/tree/gh-pages).)
- [Word](https://github.com/ismayc/thesisdown_book/blob/gh-pages/thesis.docx)
- [ePub](https://github.com/ismayc/thesisdown_book/blob/gh-pages/thesis.epub)
- [gitbook](http://ismayc.github.io/thesisdown_book)

Under the hood, the Reed College LaTeX template (and soon the Reed College Word template) is used to ensure that documents conform precisely to submission standards. At the same time, composition and formatting can be done using lightweight [markdown](http://rmarkdown.rstudio.com/authoring_basics.html) syntax, and **R** code and its output can be seamlessly included using [rmarkdown](http://rmarkdown.rstudio.com).

Using **thesisdown** has some prerequisites which are described below. To compile PDF documents using **R**, you are going to need to have LaTeX installed.  It can be downloaded for Windows at <http://http://miktex.org/download> and for Mac at <http://tug.org/mactex/mactex-download.html>.  Follow the instructions to install the necessary packages after downloading the (somewhat large) installer files.  You may need to install a few extra LaTeX packages on your first attempt to knit as well.

### Using thesisdown from Chester's GitHub

To use **thesisdown** from RStudio:

1) Install the latest [RStudio](http://www.rstudio.com/products/rstudio/download/).

2) Install the **bookdown** and **thesisdown** packages: 

```S
install.packages("devtools")
devtools::install_github("rstudio/bookdown")
devtools::install_github("ismayc/thesisdown")
```

3) Use the **New R Markdown** dialog to select **Thesis**:

![New R Markdown](thesis_rmd.png)

Note that this will currently only **Knit** if you name the directory `index` as shown above.
