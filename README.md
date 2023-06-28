# Babies MRI data report

## Summary
(leave it empty)

## Background
(leave it empty)

## Method

### Data 

In total, two important graphs were created, using python in Google Colab.

For the first graph, we selected the babies scanned between 40 weeks inclusively and 41 weeks. This represents 90 babies selected. The important data extracted to complete figure 1 are the babies' weight, the babies' scan head circumference and the babies' age. Those babies are either pretermed or normally born. With the graphs, we added error bars in order to show the incertitude of our data.

![Full graph](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/985051a0-d3f0-4bc1-b907-69c31fd55295)

The second graph correlates the birth age with the birth weight of all 489 babies. Clearly, we can see a colleration between the two variables. Hence, a regression line can be plotted in order to better vizualize the realtionship between the x and y variables.

![birth weight scatter](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/bf2739d4-372e-4ef9-9934-54bbab5404ce)


### Experiment 1: use k-means to classify the data
(explain how you did that: how many data samples? what you should do to use the k-means code? )

K-mean is an unsupervised machine that classifies the data in clusters. Its automaticity and simplycity makes it a good choice for us to classify our data. For our 489 babies, we decided to regroup them in 3 different clusters. Before using the k-mean code, first, we had to clean our data in order to drop the NA values. Then, we had to create coordinates in the type (x, y) with the datas we are interested in. For this example, we were interested in the scan head circumference and the scan age of the babies. Afterwards, we needed to create an array of the data and finally, we needed to choose the number of clusters we wanted to use.

### Results 
(show two figures of classification results; Are these results you expected? Why? Try to explain...)

![scan head circumference data](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/0541f7a1-22c3-466d-ba5a-53752391876c)

![First Model Training](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/1098fb95-3ad1-4b7a-b655-ff6d6b69a47a)

The discrepencies between those two graphs were not what we expected. The first graph was manually done based on the predefined categorizes. For the second graph, our k-means machine calculates the distances between all points on the graph and categorizes them based on their closeness. So, difference between the two figures is logical.

## Reproducibility

### Dependencies
(list the tool and library you used)
* Pandas
* Matplotlib
* Numpy
* KMeans
* Overleaf
* Markdown
* GitHub
* Google Colab

### RGB image
<img src="![119 RGB picture](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/f2a84067-abb0-445b-b494-c7cdc03883ea)" alt="drawing" width="100"/>  <img src="![409 RGB picture](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/853cb6c6-dc72-4316-aa03-8254c1355cd2)" alt="drawing" width="100"/>       
&nbsp;&nbsp; RGB figure of baby 119 in our dataset &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; RGB figure of baby 409 in our dataset

![467 RGB picture](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/b45dc16e-794a-4a77-906d-8ff00bbc67a4)    ![586 RGB picture](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/5b55f2a4-330d-4109-bd64-0b81d522942f)    
&nbsp; RGB figure of baby 467 in our dataset &nbsp;&nbsp;&nbsp; RGB figure of baby 586 in our dataset

![720 RGB picture](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/a04d84e6-9617-4ac7-a21d-08177bf1558b)    
&nbsp;&nbsp;&nbsp; RGB figure of baby 720 in our dataset
