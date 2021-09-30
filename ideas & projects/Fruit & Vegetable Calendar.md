## Summary
Calendar with info on seasonality of fruit & vegetables, based on location

## Ideas
- use google trends data in different countries for fine-grained info, maybe "xxx harvest" (translated to local language)
	- validate with existing sources of fruit x seasonality data (e.g. goodbuy calendar)
- Create calendar layout with smoothed interest over time
- Have standard calendar below, not per year, but 10 day layout?
- vgl. goodbuy seasonal calendar https://www.goodbuy.eu/collections/utopia/products/utopia-saisonkalender
- US: https://www.seasonalfoodguide.org/
- UK: https://www.bbcgoodfood.com/seasonal-calendar
- http://www.fao.org/faostat/en/#data
	- Good source of yearly-level data; globally
- EU Map: https://www.eufic.org/en/explore-seasonal-fruit-and-vegetables-in-europe

## MVP
1. Set up Rmd to donwload google trends data (there's a package I think) for different phrases
2. Type out data from goodbuy calendar for 3 types of fruit (apfel, kirsche, pflaume)
3. Compare "xxx Ernte" with data from calendar (convert trends data to binary based on > or < than mean)
