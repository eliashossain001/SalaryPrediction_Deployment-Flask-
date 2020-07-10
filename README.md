# Machine Learning Model Deployment using Flask Micro Web Framework 
This is a small project to elaborate how Machine Learn Models are deployed on production using Flask API

# Project Structure
This project has four major parts :

1. model.py - This contains code fot our Machine Learning model to predict employee salaries absed on trainign data in 'hiring.csv' file.
2. app.py - This contains Flask APIs that receives employee details through GUI or API calls, computes the precited value based on our model and returns it.
3. request.py - This uses requests module to call APIs already defined in app.py and dispalys the returned value.
4. templates - This folder contains the HTML template to allow user to enter employee detail and displays the predicted employee salary.

# Running the project
    python model.py
    
This would create a serialized version of our model into a file model.pkl

Run app.py using below command to start Flask API

    python app.py
    
By default, flask will run on port 5000.
Navigate to URL http://localhost:5000

You should be able to view the homepage as below :

![Homepage (2)](https://user-images.githubusercontent.com/54431128/87170383-17c74c00-c2f3-11ea-8add-51fbeb81b1c0.png)

Enter valid numerical values in all 3 input boxes and hit Predict.

If everything goes well, you should be able to see the predcited salary vaule on the HTML page:

![Screenshot (518)](https://user-images.githubusercontent.com/54431128/87170412-1eee5a00-c2f3-11ea-9ec1-399084b42dd4.png)

You can also send direct POST requests to FLask API using Python's inbuilt request module Run the beow command to send the request with some pre-popuated values -

    python request.py
