# SEQualyzer

The SEQualyzer (Structure-profiling Experiment Quality Analyzer ) platform allows users to visualize and quality control data from a wide range of structure profiling experiments. The user uploads a dataset containing read stop/mutation counts and local coverages (optional) from sequencing-based profiling experiments at each residue for one to few transcripts or a transcriptome. These counts are converted into reactivity scores using a reconstruction scheme chosen by the user. The quality and variability of these scores are then evaluated using several quantitative and visual metrics. Code for SEQualyzer is written in R Shiny interactive application framework and can be downloaded along with a user manual and sample datasets. 

## Citation

K. Choudhary, L. Ruan, F. Deng, N. P. Shih, and S. Aviran. SEQualyzer: Interactive
tool for quality control and exploratory analysis of high-throughput RNA structural
profiling data (in press). Bioinformatics, page btw627.

## Hardware requirements

SEQualyzer is built in native R and is platform independent. It has no specific hardware requirements and
should run on all laptop/desktop devices as long as software requirements are met.

## Launch SEQualyzer

### 1 Software requirements
SEQualyzer requires R 3.2.2 or higher and is best run with RStudio (https://www.rstudio.com/products/
rstudio/download/), an integrated development environment for R (https://www.rstudio.com/). While
there is a paid, premium version of RStudio, the open source, free version of RStudio is sufficient. The
application has been tested on MacOS X and Windows 7, and installers for these operating systems can be
found at provided link.

Users must install R 3.2.2 or higher to use SEQualyzer. To install R visit https://www.r-project.org.
To install RStudio visit https://www.rstudio.com/products/rstudio/. To upgrade R in RStudio, simply
install the right version of R. Next, change the version of R in RStudio. To read how to do that, visit https://
support.rstudio.com/hc/en-us/articles/200486138-Using-Different-Versions-of-R. Users must
install shiny package in R. It can be installed by typing

install.packages(“shiny")

and pressing enter in R Studio console. The installation needs to be done only once. For MacOS users,
SEQualyzer will attempt to install shiny on its own.

Users should be able to run SEQualyzer even without RStudio, in which case SEQualyzer will launch in
default web browser. SEQualyzer will attempt to install shiny and other packages in R. All R packages needed
for SEQualyzer are automatically installed if found missing and loaded when the application is launched.
These packages are- ggplot2, reshape2, tools, corrplot, foreach, parallel, doParallel, plyr, seqinr, rmngb , zoo
and ineq. If users experience an error when attempting to launch SEQualyzer, these packages may need
to be installed/loaded manually, using the command install.packages(). The packages can be installed by
typing

install.packages(“<insert_package_name>”)

and pressing enter in R Studio console. The installation needs to be done only once. For best experience, it
is recommended that a new session of SEQualyzer be launched for every new dataset.

### 2 General method (works on both Windows and Mac OS)
Launch RStudio and set working directory to the SEQualyzer folder. To launch SEQualyzer itself from
RStudio, just click the button “Run App” on top right of RStudio source pane. Alternatively, it can be
launched by using

shiny::runApp()

command. For other ways to launch SEQualyzer, including launching in a web browser such as Firefox,
Chrome, Safari, etc. see http://shiny.rstudio.com/reference/shiny/latest/runApp.html.

### 3 Deploying from desktop (Mac OS)
In the downloaded folder, users will find a file named "SEQualyzer.command" inside the "Code" subdirectory.
Double-clicking this file will launch SEQualyzer. Users can make an alias for this file and move
it to desktop or any desired location. The alias will launch SEQualyzer with a simple double-click. Users
might face troubles using this method if the path to SEQualyzer has a white space. Additionally, it might
be required to make the SEQualyzer.command file in "Code" folder an executable file. This can be done in
Terminal by changing the current directory to "Code" folder and using the following command.

chmod +x SEQualyzer.command

###

Refer to the user manual for instructions on input format and interpretations of output results.

## Licence
SEQualyzer is free for non-commercial research. For commercial use, please contact the authors.


