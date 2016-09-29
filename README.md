# WineQualityExplorationWithR
Use R to do exploratory data analysis on the white wine quality data.

## Some final plots

![alt tag](img/WhiteWineNbByQuality.PNG?raw=true)

The quality is a distrete. There is no extremly excellent wines (quality=10), nor extremely poor wines (quality=0, 1 or 2). Excellent wines (quality=8 or 9) and poor wines (quality=3 or 4) are also rare. Most wines are of quality 5, 6 and 7, among which the quality 6 has most number of wines, and is more than twice the number of wines of quality 7.

![alt tag](img/WhiteWineAlcoholContentOverQuality.PNG?raw=true)

For good wines (quality >= 5), the mean of alcohol content increases when the quality of white wine becomes better. However, for bad quality wines, it seems to be opposite, the mean alcohol level decreases when the quality increase. There is no much difference on variance of alcohol content for quality 6, 7 and 8.

![alt tag](img/ResidualSugarOverDensity.PNG?raw=true)

Holding residual sugar level constant, whites wines who have larger density tend to be of worse quality in general. The plot also indicates that a linear model could be constructed between residual sugar and density, and the coefficients of the model would vary following different qualities of wines.

## Reflection

What excited me most in exploring this dataset was that I succeed in builing a linear model of wine’s density by including residual.sugar and alcohol as input variables. Residual.sugar and alcohol both have a strong correlation with denstiy, so the model was not difficult to be found. However, I was struggling in creating a linear model to predict the white wine quality, and the model I built was rather poor for the prediction. I think the possible reasons for this hardness may be :

- The number of different qualities of wines is not balanced in this dataset. There are too much normal wines comparing the number of excellent wines or poor ones, which makes the analyse less reliable if we want to look into the tends towards excellent wines or poor ones.

- The quality itself is very subjective according to the evaluation system. Different wine experts could give totally different notes to the same wine. Determining a wine’s quality just by taking the median of all notes may be an approach too simple and light. In addition, the quality variable is graded on integer while all other input variables are of type float (number). This could introduce some bias as the aggregation levels of input & ouput variables are not the same. To investigate this dataset furthur and make the model better, I would perhaps include some rounding system in the quality predition model, or do some groupment of values on each input varible in order to match the quality’s aggregation level.

- The dataset only consists of wines collected from a specific portugal region. So there may be some bias created by the specfic qualities of the product of this region. It will be insteresting to analyse on a dataset accross various wine making regions.
