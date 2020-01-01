# Sentiment Analysis using Scikit-Learn and Model Deployment using Flask and Docker

Data used for this model can be found [here](https://www.kaggle.com/c/sentiment-analysis-on-movie-reviews/data)

In this section, we use TF-IDF algorithm for feature extraction from text and then applying machine learning algorithms to understand the sentiment of movie reviews. 

For understanding TF-IDF algorithm, visit my blog [here](https://hritikattri10.wordpress.com/2019/10/12/feature-extraction-using-tf-idf-algorithm/).

For understanding this project, visit my blog [here](https://hritikattri10.wordpress.com/2020/01/01/sentiment-analysis-using-scikit-learn-and-model-deployment-using-flask-and-docker/).

Then, model has been deployed using Flask. We can send requests in the following ways: 

***1) Using the command line:*** 

Open a new terminal, and enter: 

```
python app.py
```

Paste this into the terminal, and press enter.

```
curl -X GET http://127.0.0.1:5000/ -d query="i guess the movie was fine"
```

***2) Using a Python script:***

Open a new file using your IDE and paste the following code: 

```
import requests

url = 'http://127.0.0.1:5000/'
params = {'query': 'i guess the movie was fine'}
response = requests.get(url, params)
response.json()
```

***Setting up the docker container:***

To build the docker container, use: 

```
docker-compose build
```

To run it, use the following command: 

```
docker-compose up
```
