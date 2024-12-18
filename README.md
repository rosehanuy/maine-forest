# Climate-induced Changes in Northeastern Forest Composition

This project analyzes how rising annual temperatures have impacted the species composition of forests in Maine. 

## Methods
* Explore how mean annual temperatures have changed in Maine over the past fifty years. 
* Analyze relationships between annual mean temperature and tree species proportion on a county level for twelve regional tree species. 
* For the species shown to be most sensitive to temperature, map the changes in their range within Maine from 1995 to the present. 

## Data 
* Temperature data:
    * Gridded Surface Meteorological Dataset (gridMET), accessed via [Climate Engine](https://app.climateengine.com/climateEngine):  
        * mean annual air temperature from 1979-present at 4 km spatial resolution. 
    * [NOAA National Centers of Environmental Information](https://www.ncei.noaa.gov/):
        * Mean annual air temperature for each county from 1970-present.  
* Forest cover data:
    * [U.S. Forest Service Forest Inventory and Analysis Data](https://apps.fs.usda.gov/fiadb-api/evalidator):
        * Estimated acreage of tree species per county.
        * Inventory downloaded from 1995 and 2021.

## Results
This analysis visualizes how mean annual air temperatures in Maine have increased over the past 40 years. The maps below depict the mean temperatures at a 4 km spatial resolution for the years 1980, 1990, 2000, 2010, and 2020. The line graph shows annual mean temperature in each of Maine's sixteen counties from 1970 to the present. 

![gridMet map](/images/maine_temp_change.png)

![temp plot](/images/temp_change_plot.png)

To generate graphs showing the relationships between each tree species and annual temperature, I first found the fifty-year mean temperature of each county. (Data preparation notebooks can be found [here](data_prep_forest.ipynb) and [here](data_prep_temperature.ipynb)) I then plotted this fifty-year mean temperature against the species prevalence in each county. Prevalence is expressed as the percentage of total forest acreage represented by a given species. 

I found that, while most species have only a weak association with temperature, Oak and Eastern White Pine have a strong positive correlation with temperature, while Balsam Fir and Aspen have a negative correlation. 

![graphs](/images/temp_v_species_plots.png)

The final portion of this analysis shows that these four species have undergone significant changes in range within Maine since 1995. 

The cold-adapted Balsam Fir represents a smaller proportion of forests in southern counties, while its presence has increased in northern and eastern counties. Cold-loving Aspen has not migrated northward, but has simply been disappearing throughout the state.

![balsam_fir](/images/Balsam%20Fir_choropleth.png)

![Aspen](/images/Aspen_choropleth.png)

Meanwhile, warm-adapted oak and eastern white pine have been gradually increasing their presence in southern counties and even spreading further northward and eastward into the state. 

![eastern_pine](/images/Eastern%20White%20Pine_choropleth.png)

![oak](/images/Oak_choropleth.png)

This brief analysis illustrates how the known warming climate in Maine has already resulted in changes in the species composition of its forests. Some temperate species are becoming more prevalent in the state, while some boreal species are 'migrating' northward or disappearing all together. 
