# jonikas_for_weronika.-annotated-code
This is the code that might be a little useful from the analyses I ran.

heatmap of counts: In this script I clean the data then generate a heatmap of number of reads per well per plate
junk read percentage: in this script I look at the percent of junk reads in the raw data 
positional graphing: in this script I graph the relative number of readcounts across positions, showing the increased growth at the edges of the plates.
data standardization: In this script I experimented with different ways to standardize data, finally settling on scalar transformation
box plots for data range between plate ages: The point of this script was to see the data range between the different aged plates. 
                                             Some plates grew for one week from regular sized colonies, and others (after 150) grew for two weeks from very small colonies. 
                                             I wanted to see if the growth and age impacts variation. Martin later recommended I analyze it based on ratios instead.
Martin Style data analysis: Martin suggested I drop low readcounts, then create a ratio between the control and experiment, then graph them against each other. 
                           This is just me playing around with the dropped readcount data and creating various scatterplots.
Martin style final scatterplots: This is where I try to scatterplot the ratios of the condition/control data against each other in replicate and between plate ages. It fails
