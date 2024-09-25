# Geolocation-Aware Applications with Redis

This repository provides some exercises around Redis commands that are related to geospatial search.

## Preparations

1. Ensure that your computer is connected to the internet as your computer will need to access some external resources (e.g., CCS files & JavaScript UI libraries)
2. You will need access to a Redis database (Use Redis Cloud, install Redis Community Edition or run it locally via docker)
3. Clone the following code repository locally: https://github.com/redislabs-training/training-geo-public ! 
   1. This results in a local working copy of the source code.
   2. Please don’t publish the source code (e.g., by forking and pushing to a public Git repo)!
4. Prepare a Python 3.x development environment! 
      ```
      cd geoapp
      python3 -m venv geoappvenv
      source geoappvenv/bin/activate
      python3 -m pip install -r requirements.txt
      python --version
      ```
5. Configure the application to use your Redis database via the file ‘config.py’!
   1. The default configuration uses localhost and port 6379.

## Verify Setup

1. Change the directory to the source code directory ‘geoapp’!
1. Run the command  `python app.py`
1. The application listens on port 5500, so you will be able to reach it via http://localhost:5500
1. It’s expected to see the following:
   <img src="images/geoapp-init.png" width="500px">
1. Click on the link ‘Test DB Connectivity’. The expected result is:
   <img src="images/geoapp-test.png" width="500px"/>
