# R for Data Science

Setting up a repository to get folks started with Data exploration in R

## R for Data Science Book
The materials for this tutorial are extracted from the textbook, "R for Data Science" which can be found at the following link.

https://r4ds.had.co.nz/

## Setting up your environment

### Using Cheaha
1. Go to rc.uab.edu
2. log in
3. Click on Interactive Apps and then Click on Rstudio
4. Launch an instance of Rstudio
    `try to use 2 hrs, an express partition, 1 CPU, and 1 GB of RAM`
5. Run `install.packages('tidyverse')` in the Rstudio command prompt

## Cloning the repository

Use the Job Composer at https://rc.uab.edu/pun/sys/myjobs/workflows

Create a new job from the default template
Scroll down and click "Open Editor"
Copy and paste the script below into over the current contents
```
#!/bin/bash
# JOB HEADERS HERE
mkdir -p /data/user/$USER/rc-dsc

FOLDER=/data/user/$USER/rc-dsc/r-for-data-science
URL=https://gitlab.rc.uab.edu/rc-data-science/r-for-data-science.git

if [ ! -d "$FOLDER" ] ; then
    git clone "$URL" "$FOLDER"
else
    cd $FOLDER
    git pull "$URL"
fi
```
