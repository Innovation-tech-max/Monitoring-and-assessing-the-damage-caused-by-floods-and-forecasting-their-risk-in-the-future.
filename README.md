# Monitoring-and-assessing-the-damage-caused-by-floods-and-forecasting-their-risk-in-the-future.
This repo is a part of an assignment from Blue Sky Analytics . The goal is to use Python to analyze geospatial datasets and compare data across  different time periods and geographic regions to gain insights into changes in Earth- related attributes. A report of the project can be found [here]().

# **Why should I care about this topic?**

> "If you don't know where you came from, then you don't know where you are, and if you don't know where you are, then you don't know where you're going," stated English novelist Terry Pratchett. Moreover, if you don't know where you're headed, you're most likely making a mistake.

Let's go back to 2018. Due to abnormally heavy rainfall during the monsoon season, major floods hit the state of Kerala in southern India on August 16, 2018. It was Kerala's worst flood in almost a century. 
Kerala experienced a 23% over-monsoon in 2018, and in August of same year, rainfall was 96% over average. Kerala, India, saw significant rainfall on August 8 in the middle of the evening that was 116% over average, causing dams to overflow.The state got 310 mm (12 in) of rain over the last 48 hours.
When the water level had increased to almost overflow level as a result of severe rain, flooding nearby low-lying regions, nearly all dams had been opened.35 of the state's 54 dams have been opened for the first time in its history.The levelling of wetlands is thought to be one cause.The flood has been regarded as a result of global warming. 

I am from Assam and the study of floods in most of the regions can provide valuable insights and knowledge that can be applied to similar situations in my own region. Kerala and Assam share similar geographic and climatic conditions, which makes the analysis of floods in Kerala relevant and informative for understanding the potential impact of floods in Assam.


# **Goal**

The purpose of this project is to create a machine learning model capable of semantic segmentation of floodwater in order to anticipate when a flood is likely to occur, allowing early warnings to save lives and prevent flood damage. To do this, we are use the Sentinel-1 dataset, which consists of radar images recorded as 512 x 512 pixel GeoTIFFs.

The Python computer language, as well as numerous Python libraries, is being used to do detection analysis in order to assess the severity of flooding disasters. Moreover, we are attempting to discern between parts in a photograph that have floodwater and areas that do not have floodwater. This entails creating a machine learning model capable of properly segmenting floodwater zones in Sentinel-1 SAR photos.

The model will be trained on a subset of the Sentinel-1 dataset that has been manually annotated with floodwater labels. The model's performance will be measured using a variety of measures, including accuracy, precision, recall, and F1-score.

I want to create an effective tool for predicting and monitoring flood occurrences by establishing an accurate floodwater segmentation model, which can assist decrease the danger of loss of life and property damage.



# **Dataset**

The Sentinel-1 dataset was utilised to perform detection analysis and assess the severity of flooding episodes. Sentinel-1 is a satellite project created by the European Space Agency (ESA) to provide all-weather, day-and-night radar imaging to serve a variety of applications, including catastrophe monitoring and management.

The dataset utilised in this study is made up of Sentinel-1 SAR pictures spanning flood-affected areas retrieved from the Copernicus Open Access Hub. The collection consists of many acquisitions of Sentinel-1 SAR data during various time periods during and after flood occurrences, with each acquisition covering a specific area of interest. The collection includes both single and dual polarisation SAR pictures.

This project's dataset is available for download at the following site: 
(https://sentinel.esa.int/web/sentinel/user-guides/sentinel-1-sar/data-products).
The collection includes raw Sentinel-1 SAR photos as well as floodwater annotation masks.
The dataset is given in a format that is compatible with well-known machine learning frameworks like TensorFlow and PyTorch. 

#**Preprocessing**

In my analysis of Sentinel-1 GDR data for flood monitoring, I performed radiometric calibration and speckle filtering as part of the preprocessing steps. 
**Radiometric calibration** helps to correct for variations in the received signal caused by changes in the distance between the satellite and the ground surface, as well as differences in the characteristics of the radar system itself. 
**Speckle filtering** is used to reduce the impact of speckle noise, which can make it difficult to identify changes in the image over time. 
 However, I have skipped other preprocessing steps such as terrain correction, orbit file correction, and geometric calibration as in the context of flood mapping, these steps may not be necessary or may not provide significant benefits.
 
 #**Methodology**
 **1. Data Acquisition:** The Sentinel-1A Dual Polarization Ground Range Detected (GRD) High Resolution (HR) data was acquired from the European Space Agency (ESA) Copernicus Open Access Hub.

**2. Preprocessing:** The data was preprocessed to remove the radiometric and geometric distortions using Sentinel Application Platform (SNAP) software. Radiometric calibration was performed to convert the raw SAR data to backscatter coefficients, and speckle filtering was performed to reduce noise and enhance the signal-to-noise ratio.

**3. NDWI Analysis:** Normalized Difference Water Index (NDWI) was used to identify and map the water bodies. The NDWI was calculated by taking the difference between the Near-Infrared (NIR) and Shortwave Infrared (SWIR) bands and dividing it by their sum.

**4. Flood Mapping:** The NDWI output was thresholded to create a binary water mask, which was then compared with the pre-flood extent of the water bodies to identify the flooded areas. The flood map was generated using GIS software.

**5. Time Series Analysis: Finally, a time series analysis was performed to track the changes in water levels over time. The NDWI values were plotted over time for the before, during, and after flood images to identify the areas that were most affected by the flooding.

**6. Accuracy Assessment:** The accuracy of the flood map was assessed by comparing it with the ground truth data collected through field visits and high-resolution optical satellite imagery.
 
#**References**
1. Sentinel-1 Toolbox: https://sentinel.esa.int/web/sentinel/toolboxes/sentinel-1
2. Gao, B. (1996). NDWI--A normalized difference water index for remote sensing of vegetation liquid water from space. Remote Sensing of Environment, 58(3), 257-266. https://doi.org/10.1016/S0034-4257(96)00067-3
3. NDWI calculation using Python: https://www.hatarilabs.com/ih-en/normalized-difference-water-index-ndwi-with-sentinel-2-ndvi-ndre-vegetation-indices-in-python-tutorial
4. Bouaziz, S., Baghdadi, N., Zribi, M., & Lili-Chabaane, Z. (2017). Sentinel-1 InSAR coherence for urban flood monitoring: a case study of Sfax, Tunisia. Geocarto International, 32(1), 77-91. https://doi.org/10.1080/10106049.2015.1091488
5. Flood mapping using Python: https://www.hatarilabs.com/ih-en/flood-mapping-with-sentinel-1-sar-imagery-in-python-tutorial
6. Chen, C., & Wang, L. (2020). A review of remote sensing image time series analysis: from preprocessing to machine learning. Remote Sensing, 12(18), 3018. https://doi.org/10.3390/rs12183018
7. Time series analysis using Python: https://www.analyticsvidhya.com/blog/2018/02/time-series-forecasting-methods/ 


