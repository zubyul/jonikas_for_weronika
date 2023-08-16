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

HOW TO USE 

If you want to use the scripts, you will have to request the data from Weronika and then change this following part in the first box of each script to point to the location of the file in your drive.

df3 = pd.read_table(r"D:\Yuliya_test_data_table\Yuliya_test_data_table_deconv-only_3prime.txt", delimiter = '\t')#, nrows=2)

df5 = pd.read_table(r"D:\Yuliya_test_data_table\Yuliya_test_data_table_deconv-only.txt", delimiter = '\t')#, nrows=2)

I also recommend getting Anaconda3, and instead of launching jupyter directly, launching it from commandline with this command: 

jupyter notebook --NotebookApp.iopub_data_rate_limit=1.0e10

Otherwise it runs out of space to show figures for all the plates.

DATA

The data is as follows:

C1 and C2 = replicates of high CO2 condition, grown in TP in light.

R1 and R2 = replicates of regular atmosphere condition, TP in light. (Control)

D1 and D2 = replicates of regular atmosphere, dark TAP condition.

The data being used is the internal barcode, location, and read count across these experimental conditions. 3 and 5 in the code are referring to 3’ and 5’ data.

