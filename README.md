# Operationalizing Machine Learning
### **Overview**
In this project, we will continue to work with the Bank Marketing dataset. We will use Azure to configure a cloud-based machine learning production model, deploy it, and consume it. We will also create, publish, and consume a pipeline. In the end, we will demonstrate all of our work by creating a README file and a screencast video.  

## FEEDBACK- 1

The production model is being deployed to an Endpoint using “Azure Container Instance (ACI)” as the compute type
### Future Work
As part of future work, we can improvise on the below factors:
1. We could use GPU's in comparison to CPU's due to their significant speed
2. We could also use higher end of Memory Optimized CPU CLuster
3. In AutoML run We can use the allowed_models or blocked_models parameters to further, modify iterations with the available models to include or exclude
4. In AutoML while performing Classification task we could try enabling Deep Learning
5. We could also use single node AKS cluster

### **Project main steps**
In this project, we will following the below steps:
1.	Authentication
2.	Automated ML Experiment
3.	Deploy the best model
4.	Enable logging
5.	Swagger Documentation
6.	Consume model endpoints
7.	Create and publish a pipeline
8.	Documentation

## FEEDBACK- 2

## SCREENCAST LINK : https://youtu.be/xVRWRwvEzYY

## PART 1 - CONFIGURE CLOUD BASED ML MODEL & CONSUME THE MODEL

<img src="Images/pic44.PNG">

# Create and run Auto ML Experiment
### Dataset has been, created with the name “project2-demo” using the Bank Marketing dataset
<img src="Images/pic1.png">

<img src="Images/pic2.png">

### The Bank Marketing dataset is being reflecting under the Registered datasets tab

<img src="Images/pic3.png">

### Then we run the AutoML experiment & below screenshot shows the Run to be completed and the Best Model uses “Voting Ensemble” with an Accuracy of 0.91593

<img src="Images/pic4.png">

### Below screenshot shows the various algorithms that has been used along with their Accuracies

<img src="Images/pic5.png">

# Deploy the Best Model
### Best model is the one which, is on the top of the list and the algorithm is “Voting Ensemble”
<img src="Images/pic6.png">

### Best model has been, deployed using “Azure Container Instance (ACI)” & Authentication has also been enabled

<img src="Images/pic7.png">

# Enable Application Insights
### Below screenshot shows the execution summary of "logs.py" post making changes in the file 

<img src="Images/pic8.png">

### Below screenshot shows the Applications Insight URL

<img src="Images/pic9.png">

# Swagger Documentation
### Below two screenshots show that "swagger.json" file has been copied in the "swagger" directory

<img src="Images/pic10.png">

<img src="Images/pic11.png">

### Then we ensure that Docker is running and we make changes in the Port# from 80 to 9000 in the "swagger.sh" file
#### Below screenshot shows that localhost:9000 is accessible post running the "swagger.sh" file
#### After the Swagger UI container is running, we can access the website on http://localhost:9000.
<img src="Images/pic12.png">

#### On the top bar, where petsore.swagger.io shows, we change it to http://localhost:8000/swagger.json, then hit the Explore button. It now displays the content of the API for the model

<img src="Images/pic13.png">

# Consume Model Endpoints & Benchmarking
#### Then we copy the REST endpoint URL and the Primary Key from the deployed Endpoint, Consume tab and make changes in the "endpoint.py" file

<img src="Images/pic14.png">

#### Below screenshot shows the output post executing the "endpoint.py" file


<img src="Images/pic15.png">

#### A data.json file will appear after we run endpoint.py

<img src="Images/pic16.png">

#### In the provided started code, there is a benchmark.sh script with a call to ab which when executed display the below results

<img src="Images/pic17.png">

<img src="Images/pic18.png">

## PART 2 - CREATE, PUBLSH & CONSUME A PIPELINE
<img src="Images/pic45.PNG">

# Create, Publish and Consume a Pipeline
## Important libraries are imported and finally displays the SDK version

<img src="Images/pic19.png">

## Using the same configuration file we initialize the workspace

<img src="Images/pic20.png">

## Then we create the experiment with the same name which we have created earlier

<img src="Images/pic21.png">

## Then we use the existing cluster

<img src="Images/pic22.png">

## Then we use the existing data set which we have registered earlier & it displays the Basic Statistical Summary

<img src="Images/pic23.png">

<img src="Images/pic24.png">

## For training purpose we define the AutoML settings and call the AutoMLConfig class

<img src="Images/pic25.png">

## Now we create the pipeline for which we prepare the pipeline data by defining the name for the best model and location for our datastore
## Now we create the autoML step by calling the autoMLconfig

<img src="Images/pic26.png">

## Finally we create a pipeline by calling the autoML step

<img src="Images/pic27.png">

## Then we submit the pipeline

<img src="Images/pic28.png">

## Below screenshots display that the Run has been completed

<img src="Images/pic29.png">


<img src="Images/pic30.png">

<img src="Images/pic31.png">

## Finally the Pipeline execution summary is being displayed

<img src="Images/pic32.png">

## We then retrieve the best model along with it steps

<img src="Images/pic33.png">

<img src="Images/pic34.png">


<img src="Images/pic35.png">

<img src="Images/pic36.png">

## Now we test the effectiveness of the deployed model

<img src="Images/pic37.png">

## We then publish the pipeline and enable authentication locally
### We need the REST url which would be contained in the pipeline_endpoint object
#### HTTP post request is created using the endpoint URL, authentication header and the JSON file
<img src="Images/pic38.png">

## We then retrieve the Submitted pipeline run

<img src="Images/pic39.png">


<img src="Images/pic40.png">



<img src="Images/pic41.png">



<img src="Images/pic42.png">

<img src="Images/pic43.png">

# END OF PROJECT
