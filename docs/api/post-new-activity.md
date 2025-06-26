# Add an activity

In this tutorial, you learn the endpoints to call
to `POST` a new activity to a day of the week in the service.

## Before you start

Make sure you've completed the [before you begin tracking](../tutorials/before-you-begin-tracking.md) topic on the development system you'll use for the tutorial.

## What method are we using?

`POST`

## What endpoints are we using?

- List all the activities: {base-url}/activities
  
Adding a new activity to a day of the week in service requires that you use the `POST` method to store the details of the new [`activities`](activities.md) resource in the service.

## To add a new activity:

1. Make sure your local service is running, or start it by using this command, if it's not.

 ```shell

    cd <your-github-workspace>/fitness-friend/api
    json-server -w fitness-friend-db-source.json

 ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/activities`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like.

    ```js
    [
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
       }
    ]
    ```

4. In the Postman app, choose **Send** to make the request.
5. Watch for the response body, which should look something like this. Note that the names should be the same as you used in your **Request body** and the response should include the new user's `id`.

### Return body

    ```js
    [
        {

         "activity_id": 1,
         "type": "running",
         "durationMinutes": 30,
         "distanceKm": 5,
         "caloriesBurned": 300,
         "startTime": "2023-10-09T07:30:00Z",
         "endTime": "2023-10-09T08:00:00Z",
         "notes": "Morning run in the park",
         "id": 4
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


### Overview

* [Head back to the homepage](../index.md)

### Resources

* [Activities resources](./activities.md)
* [Days resources](./days.md)

### Read

* [Get all activities](./get-activities.md)
* [Get activities assigned to the days of the week](./get-days.md)

### Create

* [Add an activity resource](./post-new-activity.md)

### Edit

* [Edit a day of the week](./put-days.md)

### Delete

* [Delete an activity](./delete-activities.md)