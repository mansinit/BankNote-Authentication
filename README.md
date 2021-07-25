# Dockers

Docker commands


docker build -t money_api .

docker run -p 8000:8000 money_api

Bank authentication end to end app using Docker

1. Use the dataset from the kaggle and create a model. I've used random foret classifier. it gives 98% accuracy. It might be wrong but for now we have to focus on deploying

2. then we wil create this flask app. with one test file that we havve. we will create two html files, one for uploading and the other for retrieving  the predictions of that particular csv file.

3. You can create it as u like. If you want to create text boxes and fill the value and at the same time you need the prediction that can also be accomplished with the flask app.

4. So now after creating the app. we've a next task to dockerize this app.

5. You have to install docker on windows, since it was an enterprise version for me so it worked otherwise I've to use docker toolbox for windows.

6. then the first tsk was to pull continuum/anaconda3. So I ran this command first. docker pull continuum/anaconda3 because it was not recongnizing what is continuum. So we had to use this image. but then also the buid was failing.

7. I created this dockerfile with from copy workdir run cmd expose commands pip install reqr.txt 

8. the main issue where I was stuck was this from command, where I had no idea what to write. So earlier I was writing FROM continuumio/anaconda3:4.9.2
but then somehow I went to the docker app where I saw it was continuumio/anaconda3:latest. 

9.use the port you are using in app as your host and publish port. it doesn't matter if you expose it or not
docker run -p 3000:3000 money_api12
