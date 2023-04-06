# Monitoring-and-assessing-the-damage-caused-by-floods-and-forecasting-their-risk-in-the-future.
This repo is a part of an assignment from Blue Sky Analytics . The goal is to use Python to analyze geospatial datasets and compare data across  different time periods and geographic regions to gain insights into changes in Earth- related attributes. A report of the project can be found [here]().

# **Why should I care about this topic?**

> "If you don't know where you came from, then you don't know where you are, and if you don't know where you are, then you don't know where you're going," stated English novelist Terry Pratchett. Moreover, if you don't know where you're headed, you're most likely making a mistake.

As suggested by the quote above, we will return to 2018. Due to abnormally heavy rainfall during the monsoon season, major floods hit the state of Kerala in southern India on August 16, 2018. It was Kerala's worst flood in almost a century. 
Kerala experienced a 23% over-monsoon in 2018, and in August of same year, rainfall was 96% over average. Kerala, India, saw significant rainfall on August 8 in the middle of the evening that was 116% over average, causing dams to overflow.The state got 310 mm (12 in) of rain over the last 48 hours.

When the water level had increased to almost overflow level as a result of severe rain, flooding nearby low-lying regions, nearly all dams had been opened.35 of the state's 54 dams have been opened for the first time in its history.The levelling of wetlands is thought to be one cause.The flood has been regarded as a result of global warming. 

# **Goal**

The purpose of this project is to create a machine learning model capable of semantic segmentation of floodwater in order to anticipate when a flood is likely to occur, allowing early warnings to save lives and prevent flood damage. To do this, we are use the Sentinel-1 dataset, which consists of radar images recorded as 512 x 512 pixel GeoTIFFs.

The Python computer language, as well as numerous Python libraries, is being used to do detection analysis in order to assess the severity of flooding disasters. Moreover, we are attempting to discern between parts in a photograph that have floodwater and areas that do not have floodwater. This entails creating a machine learning model capable of properly segmenting floodwater zones in Sentinel-1 SAR photos.

The model will be trained on a subset of the Sentinel-1 dataset that has been manually annotated with floodwater labels. The model's performance will be measured using a variety of measures, including accuracy, precision, recall, and F1-score.

I want to create an effective tool for predicting and monitoring flood occurrences by establishing an accurate floodwater segmentation model, which can assist decrease the danger of loss of life and property damage.



#**Dataset**

The Sentinel-1 dataset was utilised to perform detection analysis and assess the severity of flooding episodes. Sentinel-1 is a satellite project created by the European Space Agency (ESA) to provide all-weather, day-and-night radar imaging to serve a variety of applications, including catastrophe monitoring and management.

The dataset utilised in this study is made up of Sentinel-1 SAR pictures spanning flood-affected areas retrieved from the Copernicus Open Access Hub. The collection consists of many acquisitions of Sentinel-1 SAR data during various time periods during and after flood occurrences, with each acquisition covering a specific area of interest. The collection includes both single and dual polarisation SAR pictures.

The project also includes the construction of a machine learning model capable of semantic segmentation of floodwater in addition to detection analysis. This model is being trained on a subset of the Sentinel-1 dataset that has been manually annotated with floodwater labels. This model's purpose is to anticipate when a flood will occur so that early warnings may be made to help preserve lives and prevent flood damage.

This project's dataset is available for download at the following site: 
(https://sentinel.esa.int/web/sentinel/user-guides/sentinel-1-sar/data-products).
The collection includes raw Sentinel-1 SAR photos as well as floodwater annotation masks.
The dataset is given in a format that is compatible with well-known machine learning frameworks like TensorFlow and PyTorch. 

#**Preprocessing**

#**Modelling**
#**Evaluation Metrics**
#**References**

