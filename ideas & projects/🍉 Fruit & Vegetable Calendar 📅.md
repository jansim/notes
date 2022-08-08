## Summary
Calendar with info on seasonality of fruit & vegetables, based on location

![[2D1A69D3-F2B6-4EE5-8358-F0BC5652960B.jpeg]]

## Ideas
- v1
	- Use manual data, based on calendars out there, maybe automize via the EU data or such.. would have the benefit of supporting different countries (?)
	- Create a circle corresponding to the year, inner most circle describes the month
	- Outside of the circle there's lines for each of the fruits / vegetables corresponding to the months they are active in a binary on / off fashion
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
	- Has sources for countries e.g. [Saison Kalender](https://www.regional-saisonal.de/saisonkalender-gemuese)
- icons?
	- https://www.flaticon.com/packs/fruit-and-vegetable-5?style_id=1043&family_id=260&group_id=310
 

## MVP
1. Set up Rmd to donwload google trends data (there's a package I think) for different phrases
2. Type out data from goodbuy calendar for 3 types of fruit (apfel, kirsche, pflaume)
3. Compare "xxx Ernte" with data from calendar (convert trends data to binary based on > or < than mean)
