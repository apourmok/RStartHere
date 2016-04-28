
RStartHere
==========

A guide to some of the most useful R Packages that we know about, organized by their role in data science.

[Click here to suggest packages.](https://github.com/rstudio/RStartHere/edit/master/README.Rmd)

Data Science Workflow
---------------------

Each data science project is different, but each follows the same general steps. You:

!["The data science workflow"](data-science.png)

1.  [Import](#import) your data into R
2.  [Tidy](#tidy) it
3.  Understand your data by iteratively
    1.  [visualizing](#visualize)
    2.  [tranforming](#transform) and
    3.  [modeling](#modelinfer) your data

4.  [Infer](#infer) how your understanding applies to other data sets (*including future data, i.e. predictions*)
5.  [Communicate](#communicate) your results to an audience, or
6.  [Automate](#automate) your analysis for easy reuse
7.  [Program](#program) the whole way through, since you do each of these things on a computer

Below we list the most useful R packages that we know of for each step.

Import
------

These packages help you import data into R and save data.

-   [feather](https://blog.rstudio.org/2016/03/29/feather/) - a fast, lightweight file format used by both R and Python
-   [readr](https://blog.rstudio.org/2015/10/28/readr-0-2-0/) - reads tabular data
-   [readxl](https://blog.rstudio.org/2015/04/15/readxl-0-1-0/) - reads Microsoft Excel spreadsheets
-   [openxlsx](https://github.com/awalker89/openxlsx) - reads Microsoft Excel spreadsheets
-   [googlesheets](https://github.com/jennybc/googlesheets) - reads Google spreadsheets
-   [haven](https://blog.rstudio.org/2015/03/04/haven-0-1-0/) - reads SAS, SPSS, and Stata files
-   [httr](https://blog.rstudio.org/2016/02/02/httr-1-1-0/) - reads data from web APIs
-   [rvest](https://blog.rstudio.org/2014/11/24/rvest-easy-web-scraping-with-r/) - scrapes data from web pages
-   [xml2](https://github.com/hadley/xml2) - reads HTML and XML data
-   [webreadr](https://cran.r-project.org/web/packages/webreadr/vignettes/Introduction.html) - reads common web log formats
-   [DBI](https://github.com/rstats-db/DBI) - a universal interface to database management systems (DBMS)
    -   [RMySQL](https://github.com/rstats-db/RMySQL) - MySQL driver for DBI
    -   [RPostgres](https://github.com/rstats-db/RPostgres) - Postgres driver for DBI
    -   [RSQLite](https://github.com/rstats-db/RSQLite) - SQlite driver for DBI
    -   [bigrquery](https://github.com/rstats-db/bigrquery) - Google BigQuery driver for DBI
-   [PivotalR](https://github.com/pivotalsoftware/PivotalR) - reads data from Pivitol (Greenplum) and HAWQ databases
-   [dplyr](https://github.com/hadley/dplyr) - contains an interface to common databases
-   [data.table](https://github.com/Rdatatable/data.table) - `fread()` for fast table reading

Tidy
----

These packages help you wrangle your data into a form that is easy to analyze in R.

-   [tidyr](https://github.com/hadley/tidyr) - tools for tidying layout of tabular data
-   [dplyr](https://github.com/hadley/dplyr) - tools for joining multiple tables into a tidy data set
-   [purrr](https://github.com/hadley/purrr) - tools for applying R functions to data structures, very useful when tidying
-   [broom](http://varianceexplained.org/r/broom-intro/) - turns model output into tidy data frames
-   [zoo](https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=r%20zoo) - data structures for time series data

Visualize
---------

These packages help you visualize your data.

-   [ggplot2](http://docs.ggplot2.org/current/) with [extensions](http://www.ggplot2-exts.org/) - a versatile system for making plots
    -   [ggthemes](https://github.com/jrnold/ggthemes) - plot style themes
    -   [ggmap](https://github.com/dkahle/ggmap) - maps with Google Maps, Open Street Maps, etc.
    -   [ggiraph](http://davidgohel.github.io/ggiraph/introduction.html) - interactive ggplots
    -   [ggstance](https://github.com/lionel-/ggstance) - horizontal versions of common plots
    -   [GGally](https://github.com/ggobi/ggally) - scatterplot matrices
    -   [ggalt](https://github.com/hrbrmstr/ggalt) - additional coordinate systems, geoms, etc.
    -   [ggforce](https://github.com/thomasp85/ggforce) - additional geoms, etc.
    -   [ggrepel](https://github.com/slowkow/ggrepel) - prevent plot labels from overlapping
    -   [ggraph](https://github.com/thomasp85/ggraph) - graphs, networks, trees and more
    -   [ggpmisc](https://cran.rstudio.com/web/packages/ggpmisc/) - photo-biology related extensions
    -   [geomnet](https://github.com/sctyner/geomnet) - network visualization
    -   [ggExtra](https://github.com/daattali/ggExtra) - marginal histograms for a plot
    -   [gganimate](https://github.com/dgrtwo/gganimate) - animations
    -   [plotROC](https://github.com/sachsmc/plotROC) - interactive ROC plots
    -   [ggspectra](https://cran.rstudio.com/web/packages/ggspectra/) - tools for plotting light spectra
    -   [ggnetwork](https://github.com/briatte/ggnetwork) - geoms to plot networks
    -   [ggtech](https://github.com/ricardo-bion/ggtech) - style themes for plots
    -   [ggradar](https://github.com/ricardo-bion/ggradar) - radar charts
    -   [ggTimeSeries](https://github.com/Ather-Energy/ggTimeSeries) - time series visualizations
    -   [ggtree](https://bioconductor.org/packages/release/bioc/html/ggtree.html) - tree visualizations
    -   [ggseas](https://github.com/ellisp/ggseas) - seasonal adjustment tools
-   [lattice](http://lattice.r-forge.r-project.org/) - Trellis graphics
-   [rgl](https://cran.r-project.org/web/packages/rgl/vignettes/rgl.html) - interactive 3D plots
-   [ggvis](http://ggvis.rstudio.com/) - versatile system for interactive graphs
-   [htmlwidgets](http://www.htmlwidgets.org/) - framework for creating JavaScript widgets with R
    -   [leaflet](http://rstudio.github.io/leaflet/) - Interactive maps
    -   [dygraphs](http://rstudio.github.io/dygraphs) - Interactive time series plots
    -   [plotly](https://plot.ly/r/) - Interactive plots
    -   [rbokeh](http://hafen.github.io/rbokeh) - Interactive Bokeh plots
    -   [Highcharter](http://jkunst.com/highcharter/) - Interactive Highcharts plots
    -   [visNetwork](http://dataknowledge.github.io/visNetwork) - Interactive network graphs
    -   [networkD3](http://christophergandrud.github.io/networkD3/) - Interative d3 network graphs
    -   [d3heatmap](https://github.com/rstudio/d3heatmap) - Interactive d3 heatmaps
    -   [DT](http://rstudio.github.io/DT/) - Interactive tables
    -   [threejs](https://github.com/bwlewis/rthreejs) - Interactive 3d plots and globes
    -   [rglwidget](http://cran.at.r-project.org/web/packages/rglwidget/index.html) - Interactive 3d plot
    -   [DiagrammeR](http://rich-iannone.github.io/DiagrammeR/) - Interactive diagrams
    -   [MetricsGraphics](http://hrbrmstr.github.io/metricsgraphics/) - Interactive MetricsGraphics plots
-   [rCharts](http://rcharts.io/) - many interactive JavaScript visualizations
-   [coefplot](http://github.com/jaredlander/coefplot) - visualizes model statistics
-   [quantmod](http://www.quantmod.com/) - candlestick financial charts
-   [colorspace](https://cran.r-project.org/web/packages/colorspace/vignettes/hcl-colors.pdf) - HSL based color palettes
-   [viridis](https://github.com/sjmgarnier/viridis) - Matplotlib viridis color pallete for R
-   RColorBrewer - color palettes for plots. No manual or website.
-   dichromat - color-blind friendly palettes. No manual or website.

Transform
---------

These packages help you transform your data into new types of data.

-   [dplyr](https://github.com/hadley/dplyr) - a grammar of data transformation
-   [magrittr](https://github.com/smbache/magrittr) - a concise syntax for calling sequences of functions
-   [tibble](https://github.com/hadley/tibble) - efficient display structure for tabular data
-   [stringr](https://blog.rstudio.org/2015/05/05/stringr-1-0-0/) - tools for working with strings and regular expressions
-   [lubridate](https://cran.r-project.org/web/packages/lubridate/vignettes/lubridate.html) - tools for working with dates and times
-   [xts](http://r-forge.r-project.org/projects/xts) - tools for time series based data
-   [data.table](https://github.com/Rdatatable/data.table/wiki) - fast data manipulation
-   [vtreat](https://github.com/WinVector/vtreat) - tools for pre-processing variables for predictive modeling

Model/Infer
-----------

These packages help you build models and make inferences. Often the same packages will focus on both topics.

-   stats
-   mgcv
-   lme4
-   [broom](http://varianceexplained.org/r/broom-intro/)
-   [caret](http://topepo.github.io/caret/index.html)
-   [glmnet](https://web.stanford.edu/~hastie/glmnet/glmnet_alpha.html)
-   [mosaic](http://mosaic-web.org/)
-   gbm
-   xgboost
-   randomForest
-   ranger
-   h2o
-   kernlab
-   nlme
-   ROCR
-   pROC
-   [arm](https://cran.r-project.org/web/packages/arm/index.html)
-   [glmnet](https://cran.r-project.org/web/packages/glmnet/index.html)

Communicate
-----------

These packages help you communicate the results of data science to your audiences.

-   [rmarkdown](http://rmarkdown.rstudio.com/) - easy-to-use format for reproducible reports and dynamic documents in R
-   [knitr](http://yihui.name/knitr/) - embed R code within pdf and html reports
-   [flexdashboard](http://rstudio.github.io/flexdashboard/) - easy-to-create dashboards based on rmarkdown
-   [bookdown](https://bookdown.org/) - books and long documents built on R Markdown
-   [rticles](https://github.com/rstudio/rticles) - ready to use R Markdown templates
-   [tufte](http://rstudio.github.io/tufte/) - Tufte handout R Markdown template
-   [DT](http://rstudio.github.io/DT/) - Interactive data tables
-   [pixiedust](https://github.com/nutterb/pixiedust) - Customized tables
-   [xtable](https://cran.r-project.org/web/packages/xtable/vignettes/xtableGallery.pdf) - Customized tables

Automate
--------

These packages help you create data science products that automate your analyses.

-   [shiny](http://shiny.rstudio.com/)
    -   [shinydashboard](http://rstudio.github.io/shinydashboard/)
    -   [shinythemes](http://rstudio.github.io/shinythemes/)
    -   [shinyAce](http://trestletech.github.io/shinyAce/)
    -   [shinyjs](https://github.com/daattali/shinyjs/blob/master/README.md)
    -   [miniUI](https://github.com/rstudio/miniUI)
    -   [shinyapps.io](https://www.shinyapps.io/)
    -   [Shiny Server Open Source](https://www.rstudio.com/products/shiny/shiny-server/)
    -   [Shiny Server Pro](https://www.rstudio.com/products/shiny/shiny-server/)
-   [rsconnect](http://shiny.rstudio.com/articles/shinyapps.html)
-   [plumber](http://plumber.trestletech.com/)
-   countdown
-   [rmarkdown](http://rmarkdown.rstudio.com/)
-   [rstudioapi](https://github.com/rstudio/rstudioapi)

### Program

These packages make it easier to program with the R language.

-   [RStudio Desktop IDE](https://www.rstudio.com/products/rstudio/#Desktop)
-   [RStudio Server Open Source](https://www.rstudio.com/products/rstudio/#Server)
-   [RStudio Server Professional](https://www.rstudio.com/products/rstudio/#Server)
-   [devtools](https://github.com/hadley/devtools)
-   [packrat](https://rstudio.github.io/packrat/)
-   [testthat](https://journal.r-project.org/archive/2011-1/RJournal_2011-1_Wickham.pdf)
-   [roxygen2](https://github.com/klutometis/roxygen)
-   [purrr](https://github.com/hadley/purrr)
-   [profvis](https://github.com/rstudio/profvis)
-   [rcpp](http://www.rcpp.org/)
-   [R6](https://github.com/wch/R6)
-   htmltools
-   snow
-   Rth
-   MKL by Microsoft/Revolution Analytics
-   MRS by Microsoft/Revolution Analytics
-   Arrow

Data
----

These packages contain data sets to use as training data or toy examples.

-   datasets
-   [babynames](https://github.com/hadley/babynames)
-   [neiss](https://github.com/hadley/neiss)
-   [yrbss](https://github.com/hadley/yrbss)
-   [nycflights13](https://github.com/hadley/nycflights13)
-   [hflights](https://github.com/hadley/hflights)
-   [USAboundaries](https://github.com/ropensci/USAboundaries)
-   [rworldmap](https://github.com/AndySouth/rworldmap)
-   [usdanutrients](https://github.com/hadley/usdanutrients)
-   [fueleconomy](https://github.com/hadley/fueleconomy)
-   [nasaweather](https://github.com/hadley/nasaweather)
-   [mexico-mortality](https://github.com/hadley/mexico-mortality)
-   [data-movies](https://github.com/hadley/data-movies) & [ggplotmovies](https://cran.r-project.org/web/packages/ggplot2movies/)
-   [pop-flows](https://github.com/hadley/pop-flows)
-   [data-housing-crisis](https://github.com/hadley/data-housing-crisis)
-   [gun-sales](https://github.com/NYTimes/gunsales)
-   [stationaRy](https://github.com/rich-iannone/stationaRy)
-   [ggenealogy](https://github.com/hadley/ggenealogy)
-   [ggplot2](https://github.com/hadley/ggplot2/blob/master/data/diamonds.rda)(diamonds)
-   [gapminder](https://github.com/jennybc/gapminder)
-   [janeaustenr](https://github.com/juliasilge/janeaustenr)

Criteria
--------

What makes an R Package useful? A useful R package should perform a useful task, and it should do it well. Here are some criteria that we used to make the list.

-   The code in the package runs fast, with few errors.
-   The code in the package has an intuitive syntax that is easy to remember.
-   The package plays well with other packages; you do not need to munge your data into new forms to use the package.
-   The package is widely used and recommended by its users.
-   The package has a development website, or series of vignettes, that make the package easy to learn.
-   The package is developed in the open (e.g. on Github or RForge).
-   The package uses tests to ensure that it will be stable and bug free well into the future.
-   The package is stable and available from CRAN, or we are personally involved with the package and committed to its development.

You can learn more about packages in R with the [CRAN task views](https://cran.r-project.org/web/views/).
