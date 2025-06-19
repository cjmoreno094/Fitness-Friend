# Get activities by the day of the week

In this tutorial, you learn the operations to make a call to receive details of an existing activity.

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md) topic on the development system you'll use for the tutorial.

## Request the activity

Adding a new activity to the service requires that you use the `GET` method to receive the details of the [`activities`](../api/activities.md) resource in the service.

To receive details of a specified activity:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/fitness-tracking-api/api
    json-server -w fitness-tracking-db.json
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
