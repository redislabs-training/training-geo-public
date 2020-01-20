# Training Geolocation-aware applications with Redis

## Preparations

1. Ensure that your computer is connected to the internet as your computer will need to access some external resources (e.g., CCS files & JavaScript UI libraries)
2. Prepare a Python 3.x development environment! The Python dependencies need to be installed:
   1. Flask
   2. Redis
      ```
      cd geoapp
      virtualenv --python=python3 geoappvenv
      source geoappvenv/bin/activate
      pip install -r requirements.txt
      python --version
      ```
3. Please install Redis 5.x OSS locally!
   1. No additional Redis module is required for this exercise.
4. Clone the following code repository locally: https://github.com/redislabs-training/training-geo-public ! 
   1. This results in a local working copy of the source code.
   2. Please don’t publish the source code (e.g., by forking and pushing to a public Git repo)!
5. Configure the application to use your Redis database via the file ‘config.py’!
   1. The default configuration uses port 6379.
6. Verify the database connectivity!

## Data import

1. Change the directory to the source code directory ‘geo-app’!
2. Take a look at the Python script ‘importer.py’!
3. Run the Python script ‘importer.py’ via `python importer.py`!
4. Wait until the import completes. The importer shows the message ‘Import of 16790 records completed’.
5. Which steps could be performed to speed the import up?

## Understand the source code

