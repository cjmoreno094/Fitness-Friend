# Quickstart

This tutorial shows you how to download the API files and try one of the service action to assist with tracking your activities throughout the week. 
If you've already read the [get started guide](before-you-get-started.md), the process should take about 15 minutes.

## Step 1: Check to make sure you have the API files

The directory contains the following files:

*  `fitness-tracking-db-source.json`: a JSON file containing examples of activities and how to track.
*  `fitness-tracking.sh`: a shell script that starts JSON Server. Use this for Linux or macOS.
*  `fitness-tracking.bat`: a batch file that starts JSON Server. Use this for Windows.

## Step 2: Start JSON Server

1. Open a terminal window and `cd` to the location of the json-server app.
2. Make sure the API files are in the same directory.
3. Start the service by typing `json-server -w api/fitness-database-db-source.json` into the terminal. You should see some text to show the service is running:

```
     \{^_^}/ hi!

     Loading api/fitness-tracking-db-source.json
     Done

     Resources
     http://localhost:3000/days
     http://localhost:3000/activities

     Home
     http://localhost:3000

     Type s + enter at any time to create a snapshot of the database
     Watching...
```

## Step 3: Use cURL or Postman to view activities

### Using cURL?

1. Open a new terminal window.
2. Make a test call to the service on the new terminal.

    ```
    curl http://localhost:3000/activities
    ```

### Using Postman?

1. Open Postman.
2. In the upper-right of the screen, select **GET**.
3. Add the following URL to the field next to **GET** `http://localhost:3000/activities`.
4. Click **Send**.

### Review your response

If the service is running correctly, you should see a list of users from the service, such as in this example.

```
 "activities": [
     {
       "activity_id": 1,
       "type": "running",
       "durationMinutes": 30,
       "distanceKm": 5,
       "caloriesBurned": 300,
       "startTime": "2023-10-09T07:30:00Z",
       "endTime": "2023-10-09T08:00:00Z",
       "notes": "Morning run in the park",
       "id": 1
     },
     {
       "activity_id": 2,
       "type": "cycling",
       "durationMinutes": 45,
       "distanceKm": 15,
       "caloriesBurned": 500,
       "startTime": "2023-10-10T07:30:00Z",
       "endTime": "2023-10-10T08:15:00Z",
       "notes": "Cycling around the city",
       "id": 2
     },
     { 
       "activity_id": 3,
       "type": "swimming",
       "durationMinutes": 60,
       "distanceKm": 2,
       "caloriesBurned": 400,
       "startTime": "2023-10-12T07:30:00Z",
       "endTime": "2023-10-12T08:30:00Z",
       "notes": "Swimming at the local pool",
       "id": 3
     },
     {
       "activity_id": 4,
       "type": "hiking",
       "durationMinutes": 120,
       "distanceKm": 10,
       "caloriesBurned": 800,
       "startTime": "2023-10-14T07:30:00Z",
       "endTime": "2023-10-14T09:30:00Z",
       "notes": "Hiking in the mountains",
       "id": 4
     }
   ]
       ...
   ```
In Postman, you should recieve a 200 OK message in the header above the results. 

## Next Steps

### Resources

* [Activities resources](../api/activities.md)
* [Days resources](../api/days.md)

## See Also

### Overview

* [Head back to the homepage](../index.md)

### Read

* [Get all activities](../api/get-activities.md)
* [Get activities assigned to the days of the week](../api/get-days.md)

### Create

* [Add an activity resource](../api/post-new-activity.md)

### Edit

* [Edit a day of the week](../api/put-days.md)

### Delete

* [Delete an activity](../api/delete-activities.md)