# Training Geolocation-aware applications with Redis

## Preparations

1. Ensure that your computer is connected to the internet as your computer will need to access some external resources (e.g., CCS files & JavaScript UI libraries)
2. Prepare a Python 3.x development environment! The Python dependencies need to be installed:
   a. Flask
   b. Redis
3. Please install Redis 5.x OSS locally!
   a. No additional Redis module is required for this exercise.
4. Clone the following code repository locally: https://github.com/redislabs-training/training-geo-public ! 
   a. This results in a local working copy of the source code.
   b. Please don’t publish the source code (e.g., by forking and pushing to a public Git repo)!
5. Configure the application to use your Redis database via the file ‘config.py’!
   * The default configuration uses port 6379.
6. Verify the database connectivity!
