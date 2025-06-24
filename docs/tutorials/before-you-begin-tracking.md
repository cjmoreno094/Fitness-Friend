# Before you begin tracking

## Overview

You must set up your development environment in order to use the Fitness Tracking API.

Expect this to take about 20 minutes to complete.

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
3. Enter the URL for the Fitness Tracking API: `https://github.com/cjmoreno094/fitness-friend`
4. Click **Clone**.

## !! **Test your development system**

To test your development system:.

1. Create and check out a test branch of your fork of the Fitness Tracking repository. In the below example, `<path to fitness-friend repo>` is where you cloned the **fitness-tracking-api** repository to.

   ```text
   cd <path to fitness-friend repo>
   ls
   # (see the fitnes-friend activities in the list)
   cd fitness-friend
   git checkout -b tutorial-test
   cd api
   json-server -w to-do-db-source.json
   ```

   If you installed the software correctly, you should see the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

   ```
   curl <http://localhost:3000/listActivityReferences>
   ```

3. If the service is running correctly, you should see a list of users from the service, such as in this example.

   ```
   [
       {
     "activityId": "run001",
     "type": "running",
     "durationMinutes": 30,
     "distanceKm": 5,
     "caloriesBurned": 300,
     "startTime": "2023-10-09T07:30:00Z",
     "endTime": "2023-10-09T08:00:00Z",
     "notes": "Morning run in the park",
     "userId": 1
        },
        {
     "activityId": "cycle001",
     "type": "cycling",
     "durationMinutes": 45,
     "distanceKm": 15,
     "caloriesBurned": 500,
     "startTime": "2023-10-10T07:30:00Z",
     "endTime": "2023-10-10T08:15:00Z",
     "notes": "Cycling around the city",
     "userId": 2
        },
        {
     "activityId": "swim001",
     "type": "swimming",
     "durationMinutes": 60,
     "distanceKm": 2,
     "caloriesBurned": 400,
     "startTime": "2023-10-12T07:30:00Z",
     "endTime": "2023-10-12T08:30:00Z",
     "notes": "Swimming at the local pool",
     "userId": 3
        },
        {
      "activityId": "hike001",
      "type": "hiking",
      "durationMinutes": 120,
      "distanceKm": 10,
      "caloriesBurned": 800,
      "startTime": "2023-10-14T07:30:00Z",
      "endTime": "2023-10-14T09:30:00Z",
      "notes": "Hiking in the mountains",
      "userId": 4
       ...
   ```

You should see the list of activites. If you receive an error in any step of the procedure, investigate, and correct the error before continuing. Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of activities from the service, you're ready to do the [Tutorials](INPUT HYPERLINK).
