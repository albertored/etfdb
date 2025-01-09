# etfdb

A static databse with info about ETFs available from Europe.

The database has 2 versions: a JSON one and an XML one, they both contain the same set of information but depending on your use case you may prefer one or the other.

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

## Data examples

### JSON

```json
{
    "isin": "IE00B4L5Y983",
    "asset_class": "equity",
    "wkn": "A0RPWH",
    "ticker": "EUNL",
    "name": "iShares Core MSCI World UCITS ETF USD (Acc)",
    "inception_date": "2009-09-25",
    "domicile_country": "Ireland",
    "currency": "USD",
    "hedged": "false",
    "securities_lending": "true",
    "dividends": "Accumulating",
    "ter": "0.2",
    "replication": "Optimized sampling",
    "size": "89564",
    "is_sustainable": "false",
    "number_of_holdings": "1409",
    "strategies": ["Long-only"],
    "index": "MSCI World",
    "fund_provider": "iShares",
    "sectors": [
        {
            "name": "Technology",
            "percentage": "27.21"
        },
        {
            "name": "Financials",
            "percentage": "13.84"
        },
        {
            "name": "Consumer Discretionary",
            "percentage": "10.71"
        },
        {
            "name": "Industrials",
            "percentage": "10.16"
        },
        {
            "name": "Health Care",
            "percentage": "9.97"
        },
        {
            "name": "Telecommunication",
            "percentage": "7.58"
        },
        {
            "name": "Consumer Staples",
            "percentage": "5.9"
        },
        {
            "name": "Energy",
            "percentage": "3.94"
        },
        {
            "name": "Basic Materials",
            "percentage": "3.0"
        },
        {
            "name": "Other",
            "percentage": "7.69"
        }
    ],
    "countries": [
        {
            "name": "United States",
            "percentage": "70.35"
        },
        {
            "name": "Japan",
            "percentage": "5.2"
        },
        {
            "name": "United Kingdom",
            "percentage": "3.35"
        },
        {
            "name": "Canada",
            "percentage": "2.84"
        },
        {
            "name": "Switzerland",
            "percentage": "2.48"
        },
        {
            "name": "France",
            "percentage": "2.3"
        },
        {
            "name": "Germany",
            "percentage": "2.07"
        },
        {
            "name": "Australia",
            "percentage": "1.74"
        },
        {
            "name": "Ireland",
            "percentage": "1.44"
        },
        {
            "name": "Other",
            "percentage": "8.23"
        }
    ],
    "holdings": [
        {
            "name": "Apple",
            "percentage": "4.99",
            "isin": "US0378331005"
        },
        {
            "name": "NVIDIA Corp.",
            "percentage": "4.64",
            "isin": "US67066G1040"
        },
        {
            "name": "Microsoft Corp.",
            "percentage": "4.18",
            "isin": "US5949181045"
        },
        {
            "name": "Amazon.com, Inc.",
            "percentage": "2.72",
            "isin": "US0231351067"
        },
        {
            "name": "Meta Platforms",
            "percentage": "1.74",
            "isin": "US30303M1027"
        },
        {
            "name": "Alphabet, Inc. A",
            "percentage": "1.39",
            "isin": "US02079K3059"
        },
        {
            "name": "Tesla",
            "percentage": "1.34",
            "isin": "US88160R1014"
        },
        {
            "name": "Alphabet, Inc. C",
            "percentage": "1.2",
            "isin": "US02079K1079"
        },
        {
            "name": "JPMorgan Chase & Co.",
            "percentage": "0.99",
            "isin": "US46625H1005"
        },
        {
            "name": "Broadcom Inc.",
            "percentage": "0.99",
            "isin": "US11135F1012"
        }
    ],
    "update_date": "2025-01-09",
    "holdings_update_date": "2024-11-28"
}
```

### XML

```xml
<etf>
    <isin>IE00B4L5Y983</isin>
    <asset_class>equity</asset_class>
    <wkn>A0RPWH</wkn>
    <ticker>EUNL</ticker>
    <name>iShares Core MSCI World UCITS ETF USD (Acc)</name>
    <inception_date>2009-09-25</inception_date>
    <domicile_country>Ireland</domicile_country>
    <currency>USD</currency>
    <hedged>false</hedged>
    <securities_lending>true</securities_lending>
    <dividends>Accumulating</dividends>
    <ter>0.2</ter>
    <replication>Optimized sampling</replication>
    <size>89564</size>
    <is_sustainable>false</is_sustainable>
    <number_of_holdings>1409</number_of_holdings>
    <strategies>
        <strategy>Long-only</strategy>
    </strategies>
    <index>MSCI World</index>
    <fund_provider>iShares</fund_provider>
    <sectors>
        <sector>
            <name>Technology</name>
            <percentage>27.21</percentage>
        </sector>
        <sector>
            <name>Financials</name>
            <percentage>13.84</percentage>
        </sector>
        <sector>
            <name>Consumer Discretionary</name>
            <percentage>10.71</percentage>
        </sector>
        <sector>
            <name>Industrials</name>
            <percentage>10.16</percentage>
        </sector>
        <sector>
            <name>Health Care</name>
            <percentage>9.97</percentage>
        </sector>
        <sector>
            <name>Telecommunication</name>
            <percentage>7.58</percentage>
        </sector>
        <sector>
            <name>Consumer Staples</name>
            <percentage>5.9</percentage>
        </sector>
        <sector>
            <name>Energy</name>
            <percentage>3.94</percentage>
        </sector>
        <sector>
            <name>Basic Materials</name>
            <percentage>3.0</percentage>
        </sector>
        <sector>
            <name>Other</name>
            <percentage>7.69</percentage>
        </sector>
    </sectors>
    <countries>
        <country>
            <name>United States</name>
            <percentage>70.35</percentage>
        </country>
        <country>
            <name>Japan</name>
            <percentage>5.2</percentage>
        </country>
        <country>
            <name>United Kingdom</name>
            <percentage>3.35</percentage>
        </country>
        <country>
            <name>Canada</name>
            <percentage>2.84</percentage>
        </country>
        <country>
            <name>Switzerland</name>
            <percentage>2.48</percentage>
        </country>
        <country>
            <name>France</name>
            <percentage>2.3</percentage>
        </country>
        <country>
            <name>Germany</name>
            <percentage>2.07</percentage>
        </country>
        <country>
            <name>Australia</name>
            <percentage>1.74</percentage>
        </country>
        <country>
            <name>Ireland</name>
            <percentage>1.44</percentage>
        </country>
        <country>
            <name>Other</name>
            <percentage>8.23</percentage>
        </country>
    </countries>
    <holdings>
        <holding>
            <name>Apple</name>
            <percentage>4.99</percentage>
            <isin>US0378331005</isin>
        </holding>
        <holding>
            <name>NVIDIA Corp.</name>
            <percentage>4.64</percentage>
            <isin>US67066G1040</isin>
        </holding>
        <holding>
            <name>Microsoft Corp.</name>
            <percentage>4.18</percentage>
            <isin>US5949181045</isin>
        </holding>
        <holding>
            <name>Amazon.com, Inc.</name>
            <percentage>2.72</percentage>
            <isin>US0231351067</isin>
        </holding>
        <holding>
            <name>Meta Platforms</name>
            <percentage>1.74</percentage>
            <isin>US30303M1027</isin>
        </holding>
        <holding>
            <name>Alphabet, Inc. A</name>
            <percentage>1.39</percentage>
            <isin>US02079K3059</isin>
        </holding>
        <holding>
            <name>Tesla</name>
            <percentage>1.34</percentage>
            <isin>US88160R1014</isin>
        </holding>
        <holding>
            <name>Alphabet, Inc. C</name>
            <percentage>1.2</percentage>
            <isin>US02079K1079</isin>
        </holding>
        <holding>
            <name>JPMorgan Chase &amp; Co.</name>
            <percentage>0.99</percentage>
            <isin>US46625H1005</isin>
        </holding>
        <holding>
            <name>Broadcom Inc.</name>
            <percentage>0.99</percentage>
            <isin>US11135F1012</isin>
        </holding>
    </holdings>
    <update_date>2025-01-09</update_date>
    <holdings_update_date>2024-11-28</holdings_update_date>
</etf>
```