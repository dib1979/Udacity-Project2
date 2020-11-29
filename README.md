# Operationalizing Machine Learning
### **Overview**
In this project, we will continue to work with the Bank Marketing dataset. We will use Azure to configure a cloud-based machine learning production model, deploy it, and consume it. We will also create, publish, and consume a pipeline. In the end, we will demonstrate all of our work by creating a README file and a screencast video.
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

<img src="Images/pic14.png">

<img src="Images/pic15.png">

<img src="Images/pic16.png">

<img src="Images/pic17.png">

<img src="Images/pic18.png">

# Create, Publish and Consume a Pipeline

<img src="Images/pic19.png">

<img src="Images/pic20.png">

<img src="Images/pic21.png">

<img src="Images/pic22.png">

<img src="Images/pic23.png">

<img src="Images/pic24.png">

<img src="Images/pic25.png">

<img src="Images/pic26.png">

<img src="Images/pic27.png">

<img src="Images/pic28.png">

<img src="Images/pic29.png">

<img src="Images/pic30.png">

<img src="Images/pic31.png">

<img src="Images/pic32.png">

<img src="Images/pic33.png">

<img src="Images/pic34.png">

<img src="Images/pic35.png">

<img src="Images/pic36.png">

<img src="Images/pic37.png">

<img src="Images/pic38.png">

<img src="Images/pic39.png">

<img src="Images/pic40.png">

<img src="Images/pic41.png">

<img src="Images/pic42.png">

<img src="Images/pic43.png">

# END OF PROJECT
