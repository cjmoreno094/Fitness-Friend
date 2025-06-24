# GET activities

In this tutorial, you learn the operations to call an endpoint to receive details of an existing activity.

## Before you start

Make sure you've completed read the [get started guide](before-you-get-started.md) topic on the development system you'll use for the tutorial.

## What method are we using?

`GET`

## What endpoints are we using?
•	**List all the activities**: `{base_url}/activities` <br>
•	**Get a speceific activity**: `{base_url}/activities/{activity}001` (Replace {activitiy} with the activity you want.

Search for an activity

Adding a new activity to the service requires that you use the `GET` method to receive the details of the [`activities`](../api/activities.md) resource in the service.

To receive details of a specified activity:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/fitness-friends/api
    json-server -w fitness-tracking-db-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{{base_url}}/activities/{activityId}`

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the id should be the same as you used in your **URL** as `{activityId}`.

## Return body

```js
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
  }
]
```
After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
