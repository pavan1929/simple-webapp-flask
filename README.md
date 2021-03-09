Simple Web Application
This is a simple web application docker image using Python Flask.

Below are the steps required to get this working on a base linux system.

Install all required dependencies of docker

   Start Web Server
1. Run: docker build Dockerfile -t pavan1910/simple-webapp

This comand builds the docker image using the steps in Dockerfile.
Make sure to keep app.py and Dockerfile in same folder for copy command to work.

2.It installs and Configure Web Server

The dependencies are insatlled in ubuntu environment through following commands automatically

apt-get install -y python python-pip

Installed Python Flask dependency by

pip install flask

Copies app.py

Starts web server using entrypoint command

FLASK_APP=app.py flask run --host=0.0.0.0

3. After image is builded successfully (docker images) then run
   --> docker run -p 5000:5000 pavan1910/simple-webapp
   
4. Test
Open a browser and go to URL

http://IP4address:5000                            => Welcome
   
http://IP4address:5000/how%20are%20you            => I am good, how about you?

To get the docker image, visit docker hub and search for pavan1910/simple-webapp or follow link https://hub.docker.com/r/pavan1910/simple-webapp
