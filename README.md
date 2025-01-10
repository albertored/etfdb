<a href="https://www.buymeacoffee.com/albertored" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/yellow_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

# etfdb

A static databse with info about ETFs available from Europe.

The database is available in different formats:

* `xml`
* `json`
* `csv` (splitted in multiple files)
* `xlsx`
* [Google sheet](#google-sheets)

All formats will be periodically updated.

## Included information

| Field                  | Description                                                                                          | Possible values                                                                                                                             |
| ---------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `isin`                 | International Securities Identification Number of the ETF                                            |                                                                                                                                             |
| `asset_class`          | Type of underlying ETF assets                                                                        | equity, bonds, commodities, currency, preciousMetals, realEstate, moneyMarket                                                               |
| `wkn`                  | WKN code                                                                                             |                                                                                                                                             |
| `ticker`               | Ticker                                                                                               |                                                                                                                                             |
| `name`                 | ETF full name                                                                                        |                                                                                                                                             |
| `inception_date`       | Listing date                                                                                         |                                                                                                                                             |
| `domicile_country`     | Domicile country                                                                                     |                                                                                                                                             |
| `currency`             | ETF currency                                                                                         |                                                                                                                                             |
| `hedged`               | If the ETF is currency hedged                                                                        | true, false                                                                                                                                 |
| `securities_lending`   | If the ETF lends its securities                                                                      | true, false                                                                                                                                 |
| `dividends`            | How dividends are managed                                                                            | Accumulating, Distributing                                                                                                                  |
| `ter`                  | Total Expense Ration (%)                                                                             |                                                                                                                                             |
| `replication`          | Index replication                                                                                    | Full replication, Sampling, Optimized sampling, Swap based, Swap based Unfunded, Swap based Funded, Physically backed, Physical & Synthetic |
| `size`                 | ETF size (million of EUR)                                                                            |                                                                                                                                             |
| `is_sustainable`       | If the ETF is sustainable                                                                            | true, false                                                                                                                                 |
| `number_of_holdings`   | Number of underlying holdings                                                                        |                                                                                                                                             |
| `strategies`           | ETF strategies (list)                                                                                | Long-only, Active, Short & Leverage                                                                                                         |
| `index`                | Index the ETF replicates                                                                             |                                                                                                                                             |
| `fund_provider`        | ETF provider                                                                                         |                                                                                                                                             |
| `sectors`              | Sectors distribution, for each sector you find the name and the ETF percentage on that sector        |                                                                                                                                             |
| `countries`            | Countries distribution, for each country you find the name and the ETF percentage on that country    |                                                                                                                                             |
| `holdings`             | Top holdings of the ETF, for each holding tou find the name, the ETF percentage and the holding ISIN |                                                                                                                                             |
| `update_date`          | Last update date                                                                                     |                                                                                                                                             |
| `holdings_update_date` | Last holdings, sectors and countries update date                                                     |                                                                                                                                             |

## Google Sheets

In addition to the `xlsx` file included in the repository, it is also availbale a
[public Google Sheet](https://docs.google.com/spreadsheets/d/1SxnXVC6o6DGhCMJvmhvgS3FMLhwwAKyoK5o-OQUdcl4/edit?usp=sharing)
with all the ETF database alredy imported.

The sheet is composed of 5 different sheets:

* *basic-info*, *sectors*, *countries*, *holdings* are auto explicative and correspond to the `csv` files with the same name included in the repo
* *examples* is a sheet where some custom named formulas are used to extract data from other sheets.

This sheet will remain public and you can use it to import data on your personal file.
It can be done by defining your own formula (using [Google `IMPORTRANGE`](https://support.google.com/docs/answer/3093340))
or by using the ones already defined in the sheet:

* `ETF_BASIC_INFO(url, isin, field)`
* `ETF_SECTOR(url, isin, sector)`
* `ETF_COUNTRY(url, isin, country)`

This formulas can be easily defined on your personal sheet by going to *Data > Named functions > Import function* and selecting the
sheet linked above.

## Contributing

If you have any suggestion on how to improve the project feel free to open an issue.

In case some info are missing, wrong, outdated open an issue using the corresponding issue template.