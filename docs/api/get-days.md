# GET days

In this tutorial, you learn the operations to call 
an endpoint to `GET` details about an activity for 
a specific day of the week.

## Before you start

Make sure you've completed read the [get started guide](before-you-get-started.md) topic on the development system you'll use for the tutorial.

## What method are we using?

`GET`

## What endpoints are we using?

- List all the activities: `{base_url}/days` <br>
- Get a speceific activity: `{base_url}/days/{id}` (Replace {id} with the number associated with day of the week you'd like to view.)

## Search for a day of the week

Searching for the day of the week in the service requires that you use the `GET` method to receive the details of the [`days`](../api/days.md) resource in the service.

To receive details of a specified activity:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/fitness-friends/api
    json-server -w fitness-tracking-db-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{{base_url}}/days/{id}`

4. In the Postman app, choose **Send** to make the request.
5. Watch for the response body, which should look something like this. Note that the id should be the same as you used in your **URL** as `{activity_id}`.

### Return body

```js
[
    {
    "day": "Monday", 
    "activity": "Y",
    "activityId": 1,
    "id": 1
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

## Next Step

### Edit

* [Edit a day of the week](./put-days.md)

## See Also

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

### Delete

* [Delete an activity](./delete-activities.md)