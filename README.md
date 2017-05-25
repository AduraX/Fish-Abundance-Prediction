# FISH ABUNDANCE ANALYSIS
## Adura ABIONA, PhD (UNSW)
### 4 May, 2017

## Introduction
This project is based on data from ABARES within Australian Department of Agriculture and Water Resources. This data describes a hypothetical, but plausible fishery, targeting babelfish.
### Short Description for the Required Task
A regular analysis performed with this type of data is a regression to associate catch rate with time.  The underlying assumption being that the amount of fish caught per unit of fishing effort will be proportional to the abundance of fish.  Regression method is often used to analyse this type of data. Present a description of your data preparation, including cleaning and data summary; the results of your model(s) and interpretation; and some of your thoughts on how to visualise this type of information for a non-technical audience. 
 
### Dataset Information
Fisheries data is based on data collected by crew member on the vessel. As such it contains errors and many idiosyncrasies. Most of these have been removed from the dataset provided but some still remain. The dataset provided consists of 47851 rows and 11 columns/fields. A description of each field follows:
* **Year, Month**: self-explanatory
* **Vessel_ID**: the fishing fleet consist of many vessels, each vessel is assigned a unique ID
* **Catch_kg**: the weight of the catch on each occasion
* **Long**: longitude
* **Lat**: latitude
* **Depth**: the depth in metres
* **DayNight**: here is an example of idiosyncrasies, there are 4 entries “D”,”M”,”N”,”U”.
* **Effort_hr**: the hours spent in taking the catch on each occasion

The catch rate or Catch per Unit of Effort (CPUE) is the catch per unit of effort over a time interval and defined:
\begin{equation*}
CPUE = \frac{C}{F} = q . B
\end{equation*}
***C = Catch(Kg),  F = Effort over time (hours), B = Population Abundance, q = Catchability***

From the details given on the features and the equation above, to analyse population abundance I will undertake catch prediction using regression method based on gradient boosted decision trees.