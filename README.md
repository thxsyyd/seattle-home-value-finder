# Seattle Home Value Finder

Which homes in King County, Washington sold for less than a price model expected?

**Live map: https://thxsyyd.github.io/seattle-home-value-finder/**

A single-page map of 21,612 home sales recorded in King County between May 2014
and May 2015. A linear regression model estimates what each home should have sold
for from its size, grade, age and location; sales that came in below that estimate
are flagged as possibly undervalued.

These are past sales, not listings. Nothing here is for sale, and nothing here is
financial advice.

## Using it

- **Price range, square feet, home age** take a minimum and a maximum. Leave either
  side blank for no limit. Prices accept `300000`, `300k`, `$1.2m` and so on.
- The histogram above the price inputs shows where the sales actually sit, so you can
  see whether your range covers many homes or few.
- **All Homes** colours each zipcode by its average price per square foot; green is
  cheaper. **Undervalued Homes** shows only the 1,473 sales that came in below the
  model's estimate.
- The **?** button on the map explains what the data covers, how the estimate is made,
  and how far it can be trusted.

## What is in this repository

| File | |
|---|---|
| `index.html` | the page: layout, map, filters |
| `v5-sales.js` | the 21,612 sales and the 1,473 flagged as undervalued |
| `v5-bounds.js` | zipcode boundaries, full precision from the Census ZCTA shapes |

Data files load as plain scripts rather than `fetch()`, so the page also works when
opened straight from disk, with no server.

## Credits

- Home sales: [House Sales in King County, USA](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction) (Kaggle)
- Zipcode boundaries: U.S. Census Bureau ZIP Code Tabulation Areas
- Base map: Esri Light Gray Canvas; rendering by [Leaflet](https://leafletjs.com/)

## Licence

[CC BY-NC-ND 4.0](LICENSE) — you may view and share this with credit, but not
use it commercially, publish modified versions, or submit it as your own
coursework.
