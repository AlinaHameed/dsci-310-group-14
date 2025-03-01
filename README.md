# Project: COVID-19 Anxiety Trend Analysis
- The list of contributors/authors: 
    - Alina Hameed
    - Vincy Huang
    - Alan Lee
    - Charlotte Ren
- A short summary of the project:
    **This project investigates whether an increase in newly hospitalized COVID-19 patients and a lower vaccination count lead to higher anxiety search trends. The analysis uses publicly available data and applies regression to explore potential correlations.**

### How to run our data analysis?
To reproduce the analysis in a containerized environment, please follow the following steps:
1. Clone and move into the current Github repository with the following commands in bash into your local working directory:
```
git clone https://github.com/UBC-DSCI/dsci-310-group-14.git
```
```
cd dsci-310-group-14
```
2. Set up the environment using Docker image (based on Docker image `tidyverse` 4.4.3):

(Please first make sure the `Docker` application is opened and running in the background)

```
docker build -t covid_analysis .
```
```
docker run --rm -it -p 8888:8787 -v /$(pwd):/home/rstudio covid_analysis
```
3. Access analysis:
    Open a browser and go to http://localhost:8888.

    Enter 'rstudio' as the username and the password from the output of previous `docker run` command to open our Rstudio container.

    From the `Files` panel of the Rstudio, open `covid_analysis.qmd` from the root folder. You can run our analysis by running `covid_analysis.qmd`.

- A list of the dependencies needed to run the analysis, given the `rocker/tidyverse:4.4.3 image`:
  - remotes
  - tidymodels (version 1.3.0)
  - GGally (version 2.2.1)
  - tidyverse (pre-installed in rocker/tidyverse image)

- The names of the licenses contained in `LICENSE.md`

  Project Code: Licensed under the MIT License.
  
  Report and Documentation: Licensed under Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International.
