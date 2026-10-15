# INFO2950

This INFO 2950 project combines a family business's hat sales and product catalog with NOAA monthly climate data. Our research question is: **How are contiguous U.S. monthly temperature and precipitation associated with the business's monthly hat sales, and does the relationship differ by hat material?**

## Group Members

- William Chen wc724
- May Wu zw757
- Clément Rozé cpr58
- Joshua Chen jc3852

## Phase 2

See [the Phase 2 notebook](phase2.ipynb) for the research question, data cleaning, data description, limitations, preliminary exploratory analysis, draft preregistration statements, and reviewer questions.

Open the notebook with a Python environment containing pandas, matplotlib, and IPython. Run all cells from the repository root, review the marked TODOs, and export the executed notebook as one PDF for Gradescope. The notebook now loads both NOAA files, converts their units, and merges national weather with monthly sales. Sales export completeness and material classifications still need verification before the planned analyses can be performed.

**NOAA import and merge are complete:** all 813 observed month–material rows have both weather values. The notebook includes saved outputs from all 15 code cells, sales and weather plots, and updated written interpretations. The proposed regressions have not been run.
  
## Family business

The link is here: https://angelawilliam.com/

## Datasets

1. **Sales transactions:** Invoice lines, including the date, item, quantity, sales price, and amount, plus report headings and subtotals that are removed during cleaning.
2. **NOAA monthly weather:** `csvs/TempreatureData.CSV` and `csvs/PrecipitationData.CSV`, downloaded from the [NOAA nClimDiv directory](https://www.ncei.noaa.gov/monitoring-content/data/us/climdiv/monthly/current/). The notebook selects the contiguous U.S. series (region 110, lower 48 states). These files contain space-separated text despite their `.CSV` extension.
3. **Product information:** Item IDs, catalog types, descriptions, and prices. Material is inferred provisionally from description words; it is not a verified structured field.

## Data Availability
The business data are existing accounting exports. The supplied sales report contains invoice dates from October 1, 2006 through August 13, 2026. That date range does not establish complete transaction coverage. NOAA files have also been downloaded and added locally, so collection does not run inside the notebook.

The business exports are private source data. The NOAA data are public and are documented in the [statewide/regional/national format guide](https://www.ncei.noaa.gov/monitoring-content/data/us/climdiv/monthly/current/state-readme.txt). The notebook reads the local files, so no API calls are needed when running it. Record the original NOAA release filenames and download date before submission.

## Data Trustworthiness
The business records come directly from its accounting system. We still need to confirm export filters, quantity units, and whether recording practices changed over time. NOAA documents how it checks station observations and creates area-weighted climate estimates in the format guide linked above. These documented procedures support use of the climate series, although national averages may not represent customers' local weather.



## Limitations
- Product descriptions, particularly colors, are not always standardized. For example, similar straw colors may be recorded as "raffia," "natural," or "beige," and some entries may contain spelling variations.
- The notebook has cleaned and aggregated positive candidate-hat invoice quantities by month and material. These quantities are provisional gross sales, not verified net sales after returns.
- Both transaction reports contain exactly 32,768 data rows and end within a group, suggesting a possible export limit that needs verification.
- Unknown or ambiguous material accounts for 91.9% of retained quantity, so material labels need substantial review.
- The NOAA series represents the lower 48 states, not each customer's location. Complete weather coverage does not establish complete sales coverage.


<img width="680" height="573" alt="image" src="https://github.com/user-attachments/assets/245ae870-eeec-4ed3-b00a-312714e04b01" />
