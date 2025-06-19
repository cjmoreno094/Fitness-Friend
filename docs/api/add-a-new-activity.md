# Tutorial: Add a new activity

In this tutorial, you learn the operations to call to
add a new activity for a user of the service.

## Before you start

Make sure you've completed the [Before you start a tutorial](tutorials/before-you-begin-tracking.md) topic on the development system you'll use for the tutorial.

## Add a new activity

Adding a new activity to the service requires that you use the `POST` method to store the details of the new [`activities`](api/activities.md) resource in the service.

To add a new activity:

1. Make sure your local service is running, or start it by using this command, if it's not.

     ```shell
    cd <your-github-workspace>/fitness-tracking-api/api
    json-server -w fitness-tracking-db.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/activities`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like.

        ```js
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
        }
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the names should be the same as you used in your **Request body** and the response should include the new user's `id`.

    ```js
    {
       "activityId": "cycle001",
       "type": "cycling",
       "durationMinutes": 45,
       "distanceKm": 15,
       "caloriesBurned": 500,
       "startTime": "2023-10-10T07:30:00Z",
       "endTime": "2023-10-10T08:15:00Z",
       "notes": "Cycling around the city",
       "userId": 3
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
