COVID19 Analysis by @averissimo
================

> Exploratory analysis of worldwide COVID-19 cases/deaths.

The full analysis can be found in one of the links below and is updated
as the data is updated.

  - [World](https://averissimo.github.io/covid19-analysis/)
  - [Germany](https://averissimo.github.io/covid19-analysis/germany.html)
    *(by state)*
  - [Italy](https://averissimo.github.io/covid19-analysis/italy.html)
    *(by regione)*
  - [Bavaria](https://averissimo.github.io/covid19-analysis/bayer.html)
    *(Germany)*

Analysis by age group:

  - [Germany](https://averissimo.github.io/covid19.de.data/) *(by
    district)*

### Source code and tecnhology

Source code is available at
[averissimo/r-analysis-covid19](https://github.com/averissimo/r-analysis-covid19).
All the data and analysis was processed in [R programming
language](https://www.r-project.org/).

Data is retrieved from official sources and they are usually updated
once or twice every 24h. The report itself is updated every 15minutes,
even if there are no changes in the data.

#### Data

World data is retrieved from [EU
CDC](https://data.europa.eu/euodp/en/data/dataset/covid-19-coronavirus-data)
and is used as the main data source. When there is a delay on the
release, we alternatively use [John
Hopkin’s](https://github.com/CSSEGISandData/COVID-19/).

Currently, the only exception is for Portugal’s data, which is updated
around noon *(local time)* and we extract that information directly from
the daily situation [PDF
report](https://covid19.min-saude.pt/relatorio-de-situacao/) and store
the updated dataset in a data package
[averissimo/covid19.pt.data](https://github.com/averissimo/covid19.pt.data).

**Notes**

Data is mainly from EU CDC with some updates from Italy, Portugal and
Germany’s institutes responsible with this pandemic.

We also use Eurostat and World Bank for relevant statistics and
populations.

Mapping for Italy codici\_regione taken from
[istat](https://www.istat.it/it/archivio/6789) *(note: two regions are
mapped to same NUTS 2, we chose one – see `download.it.data`)*

Badge showing problems with report generation:
![<https://github.com/averissimo/covid19-analysis/actions>](https://github.com/averissimo/covid19-analysis/workflows/.github/workflows/main.yml/badge.svg)

## Some Interesting plots

These are included in the full analysis. They are showing data for a
select group of countries.

### Death / Confirmed cases rate

Percentage shows the Death rate per cases. Size of circle represents the
size of the population.

![](https://averissimo.github.io/covid19-analysis/index_files/figure-html/main_plots_death_cases-1.svg)

### Rolling average of past 4 days

Each data point is an average of the previous 4 days
![](https://averissimo.github.io/covid19-analysis/index_files/figure-html/main_plots_last_week_cumulative_confirmed-1.svg)

### Rolling average of deaths *(per 100k population)*

Each data point is an average of the previous 4 days

![](https://averissimo.github.io/covid19-analysis/index_files/figure-html/main_plots_last_week_cumulative_deaths-1.svg)
