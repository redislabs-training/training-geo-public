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

1. Open the file ‘app.py’ with an editor of your choice!
2. Read and understand the source code!
   1. The file is just 125 lines of code long.


## Implementation tasks

The idea of this exercise is to complete 5 simple implementation tasks. The surrounding source code is given, which should allow you to focus on the Redis commands. Each task is marked within the source code (e.g., `# Task 1 … <Your code here!>`.

### Task 1 - Scan for a city with a specific name prefix

1. You will need to identify the relevant index within the database. Indexes are prefixed with ‘idx’.
2. Please assign the result of the command to the variable ‘rs’! This variable should have the type of an ‘iterator’. The Redis-side cursor-based iteration is already implemented by the client library.

### Task 2 - Retrieve the country of the city

1. The country should be retrieved as a Python string value, and it should be assigned to the variable with the name ‘country’.
2. You can verify if Task 1 and Task 2 returned a valid result by looking at the debug output: `DEBUG: id = {}, city = {}, country = {}`

### Task 3 - Retrieve the coordinates of the city

1. You will need to identify the index within the database, which holds the geo-coordinates of cities.
2. The result of the command should be assigned to the variable ‘pos’

### Task 4 - Find max. 10 close-by breweries

1. The previously fetched city coordinates can be leveraged for finding close-by breweries.
2. You will also need to use the distance variable (dist), which was passed over as a request parameter. The distance is considered to be in miles.
3. Please construct your command in a way that ...
    1. you are NOT fetching the exact distance of resulting brewery.
    2. you are fetching the coordinates of a resulting brewery.
    3. a maximum of 10 breweries are returned (it might be otherwise hard to  draw more than 10 on a map).
4. The result-set should be assigned to the variable ‘brewcoords’.

