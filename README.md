## Project Overview

The purpose of this project is to explore the effect of higher- or lower-than-expected CPI data releases on U.S. rates and CPI swaps.

## Steps Involved:

- Extract data from the Bloomberg Terminal using the API and import it into Excel.
- Define CPI Survey Delta (% chg) as the difference between the actual data release (given by Bloomberg) and Bloomberg's survey estimate of Wall Street’s forecast:
  - The CPI Survey Delta (% chg) is an actual data release meaning that it is a better comparison of the historic market reaction to CPI on the given release date (apples-to-apples comparison).
  - A positive CPI Survey Delta (% chg) means the change in CPI was higher than forecasted by Wall Street.
    - This can indicate higher inflation, potentially causing rates/swaps to sell off.
  - A negative CPI Survey Delta (% chg) means the change in CPI was lower than forecasted by Wall Street.
    - This can indicate lower inflation, potentially causing rates/swaps to rally.
- Define CPI Survey Delta (index) as the difference between the adjusted data release (calculated from the index) and Bloomberg's survey estimate of Wall Street’s forecast:
  - The CPI Survey Delta (index) is an adjusted data release meaning that it is a poorer comparison of the historic market reaction to CPI on the given release date (apples-to-oranges comparison).
  - A positive CPI Survey Delta (index) means the change in CPI was higher than forecasted by Wall Street.
    - This can indicate higher inflation, potentially causing rates/swaps to sell off.
  - A negative CPI Survey Delta (index) means the change in CPI was lower than forecasted by Wall Street.
    - This can indicate lower inflation, potentially causing rates/swaps to rally.
- Calculate the 10-Year basis point (bps) Delta as the daily change in the 10-Year U.S. Treasury yield (USGG10YR Index) on the release date.
  - Date range: 01/14/2000 - 01/15/2025
- Calculate the 2-Year basis point (bps) Delta as the daily change in the 2-Year U.S. Treasury yield (USGG2YR Index) on the release date.
  - Date range: 01/14/2000 - 01/15/2025
- Calculate the 10-Year CPI Swaps bps Delta as the daily change in the 10-Year CPI swaps yields (USSWIT10 BGN Curncy) on the release date.
  - Date range: 08/17/2004 - 01/15/2025 (constrained start date due to data availability)
- Calculate the 2-Year CPI Swaps bps Delta as the daily change in the 2-Year CPI swaps yields (USSWIT2 BGN Curncy) on the release date.
  - - Date range: 08/17/2004 - 01/15/2025 (constrained start date due to data availability)
- Load the Excel data into Python for further analysis.
- Use Pandas to manipulate and explore the data.

## Current Findings:

- 2-Year Treasury Yield: Yield changes on CPI release days tend to be positive with higher-than-expected releases and negative with lower-than-expected releases, aligning with the above-outlined relationship.
- 10-Year Treasury Yield: Yield changes on CPI release days tend to be positive with higher-than-expected releases and negative with lower-than-expected releases, aligning with the above-outlined relationship.
- 2-Year CPI Swaps Yield: Yield changes on CPI release days tend to be positive with higher-than-expected releases and negative with lower-than-expected releases, aligning with the above-outlined relationship.
- 10-Year CPI Swaps Yield: Yield changes on CPI release days tend to be positive with higher-than-expected releases and negative with lower-than-expected releases, aligning with the above-outlined relationship.
- Generally, CPI swaps have a stronger relationship with both measurements of CPI Survey Delta than U.S. rates.
- For most data series, as the spread of data increases a stronger correlation is observed.
