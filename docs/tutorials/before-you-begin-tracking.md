# Before you begin tracking

## Overview

You must set up your development environment in order to use Fitness Friend.

Expect this to take about 20 minutes to complete.

![Screenshot 2025-07-02 at 9 00 45 PM](https://github.com/user-attachments/assets/7d96d5be-667e-4484-a1f8-408236def49c)

## Step 1: Create a GitHub user account

You’ll need a GitHub account. If you don’t already have one, create one at [GitHub](https://github.com/).

## Step 2: Install the required software

Install the following software on your desktop, which should run a recent version of Windows, macOS, or Linux.

- **[GitHub Desktop](https://github.com/apps/desktop)**
- A recent version of **[node.js](https://nodejs.org/en)**
- A recent version of **[json-server](https://www.npmjs.com/package/json-server)**
- A current copy of the **database file** and the relevant **startup script**. You can get these by syncing your fork. They’re located in the `/api` directory.
- The [**Postman desktop app**](https://www.postman.com/downloads/). You’ll run the Fitness Friend service on your development system with an `http://localhost` host name, so the web version of Postman won’t work.

## Step 3: Fork the repository

1. Go to https://github.com/cjmoreno094/fitness-friend.
2. Click the **Fork** button on the right side of the page, near the top.

## Step 4: Clone the repository

Using GitHub Desktop, clone a repository to the workspace on your desktop.

1. Go to **File** > **Clone Repository**.
2. Select the **URL** tab.
3. Enter the URL for Fitness Friend: `https://github.com/cjmoreno094/fitness-friend`
4. Click **Clone**.

## Step 5: Test your system

Create and checkout a test branch of your fork of the fitness-friend repo. 

To download each file:
1. Move your cursor over the filename and select the link that appears.
2. Locate the download button on the top right corner of the panel, indicated by a down arrow, and click it.
3. Repeat this process for the `fitness-tracking-db-source.json` file and one of the startup scripts: `start-server.sh` for macOS and Linux or `start-server.bat` for Windows.

## Step 3: Run the JSON server

1. Navigate to the directory where you downloaded fitness-tracking-db-source.json and the start scripts.
2. On Windows, double-click the `start-server.bat` file to start the service. On macOS or Linux, open the terminal, `cd` <directory name> where you downloaded the files, and type `./start-server.sh`. That runs the script in the current directory. If that doesn’t work, type `json-server -w api/fitness-tracking-db-source.json`. You should see some text to show the service is running:

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

3. If your development system is installed correctly, you should see the service start and display the URL of the service: `http://localhost:3000`.
4. Open a new terminal.
5. Make a test call to the service on the new terminal.

    ```
    curl http://localhost:3000/activities
    ```
6. If the service is running correctly, you should see a list of users from the service, such as in this example.

```
[
  {
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
  }
]
  ```

### Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |


After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.

If you receive an error in any step of the procedure, investigate, and correct the error before continuing. Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

## Next Steps

If you see the list of activities from the service, you're ready to move on to the [quickstart guide](quickstart.md).


## See Also

### Overview

* [Head back to the homepage](../index.md)
