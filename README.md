# Google Machine Learning
In this lab we are going to analyze a large (70 million rows, 8 GB) airline dataset using Google BigQuery and Cloud Datalab.
This exercise will have these steps:-

Launching Cloud Datalab
Invoking a BigQuery query
Creating graphs in Datalab

We will aggregate the original data in BigQuery, to get back a Pandas dataset and then will work with the smaller Pandas dataset locally. The Google Cloud Datalab provides a managed Jupyter experience for coding and showing the results.

Firstly, we will ensure the Cloud Source Repositories API is enabled: 
https://console.cloud.google.com/apis/library/sourcerepo.googleapis.com/?q=Repositories

**Launch Cloud Datalab**  
Open Cloud Shell and follow these steps:-
1. gcloud compute zones list 
2. datalab create mydatalabvm --zone <ZONE>( Type in the zone name ) 

**Invoke BigQuery**
Navigate to the BigQuery console by selecting BigQuery on Google Cloud Platform menue.
Now we will create a query using BigQuery console

*Query code*  
#standardSQL  
SELECT   
  departure_delay,   
  COUNT(1) AS num_flights,   
  APPROX_QUANTILES(arrival_delay, 5) AS arrival_delay_quantiles   
FROM   
  `bigquery-samples.airline_ontime_data.flights`   
GROUP BY      
   departure_delay   
HAVING     
   num_flights > 100   
ORDER BY     
   departure_delay ASC   
 
 
  
  
