# (put tittle here)
Neuroscience Internship


## Summary
(leave it empty)

## Background
(leave it empty)

## Method

### Data 

In total, two important graphs were created, using python in Google Colab.

For the first graph, we selected the babies scanned between 40 weeks inclusively and 41 weeks. This represents 90 babies selected. The important data extracted to complete figure 1 are the babies' weight, the babies' scan head circumference and the babies' age. Those babies are either pretermed or normally born. With the graphs, we added error bars in order to show the incertitude of our data.

![Full graph](https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/423e3438-9fe1-4725-8b34-b56e875914f7)

The second graph correlates the birth age with the birth weight of all 489 babies. Clearly, we can see a colleration between the two variables. Hence, a regression line can be plotted in order to better vizualize the realtionship between the x and y variables.

<img width="534" alt="Screen Shot 2023-06-18 at 9 31 23 AM" src="https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/60fd48d0-71f4-4816-87c2-1b4d5d636aac">


### Experiment 1: use k-means to classify the data
(explain how you did that: how many data samples? what you should do to use the k-means code? )

K-mean is an unsupervised machine that classifies the data in clusters. Its automaticity and simplycity makes it a good choice for us to classify our data. For our 489 babies, we decided to regroup them in 3 different clusters. Before using the k-mean code, first, we had to clean our data in order to drop the NA values. Then, we had to create coordinates in the type (x, y) with the datas we are interested in. For this example, we were interested in the scan head circumference and the scan age of the babies. Afterwards, we needed to create an array of the data and finally, we needed to choose the number of clusters we wanted to use.
The code for k-mean looks like this:
    from sklearn.cluster import KMeans
    E = df1[['scan_head_circumference', 'scan_age']].values
    X = np.array(E)
    kmeans = KMeans(n_clusters=3, random_state=0, n_init="auto").fit(X)
    kmeans.labels_

### Results 
(show two figures of classification results; Are these results you expected? Why? Try to explain...)

<img width="555" alt="Screen Shot 2023-06-18 at 9 47 36 AM" src="https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/e1f35031-e100-46dc-b776-4adf48f09eb6">

<img width="512" alt="Screen Shot 2023-06-18 at 9 48 23 AM" src="https://github.com/kyliexxu/dMRI_data_analysis/assets/135480679/a07e383b-d453-40b4-a6b6-946b8d09be5c">

The discrepencies between those two graphs were not what we expected. The first graph was manually done based on the predefined categorizes. For the second graph, our k-means machine calculates the distances between all points on the graph and categorizes them based on their closeness. So, difference between the two figures is logical.

## Reproducibility

### Dependencies
(list the tool and library you used)
* Matplotlib.pyplot
* Numpy
* Overleaf
* Markdown
* GitHub
* Google colab



