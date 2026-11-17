# Natural Gas Prices and Retail Electricity Costs

DSAN 5100 final project. We study how swings in natural gas prices affect retail electricity prices, and how the speed and size of the effect vary by state and sector.

Team: Anand Blum, Petra Chuenarrom, Marco Da Santos Manziano, Michael Taglia

## Run it

1. Use the R and Quarto setup from class (`tidyverse` and `plotly` are already part of it). One extra package is needed: `install.packages("tseries")`, for the ADF and KPSS tests.
2. Render: `quarto render gas_electricity_project.qmd`

The data is cached in `data/raw/`, so no API key is needed to render.

To refresh the data, delete everything in `data/raw/` and render again. Retail prices and generation come from the EIA API and need a free key (https://www.eia.gov/opendata/register.php). Copy `.Renviron.example` to `.Renviron` and add your key. Henry Hub and the CPI are downloaded without a key.

## Layout

- `gas_electricity_project.qmd`: main document, pulls in the section files
- `sections/01_data.qmd`: data pull, cleaning, inflation adjustment, join
- `sections/02_eda.qmd`: general exploratory analysis and findings
- `sections/03_hypothesis.qmd`: spike definition and H1
- `sections/04_timeseries.qmd`: series specific EDA (decomposition, ACF, lag plots) and stationarity tests
- `data/`: cached raw pulls and the joined monthly dataset
- `proposal/`: the submitted proposal
