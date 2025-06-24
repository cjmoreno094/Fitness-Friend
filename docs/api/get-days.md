# GET days

In this tutorial, you learn the operations to call an endpoint to receive details about an activity for a specific day of the week.

## Before you start

Make sure you've completed read the [get started guide](before-you-get-started.md) topic on the development system you'll use for the tutorial.

## What method are we using?

`GET`

## What endpoints are we using?
•	**List all the activities**: `{base_url}/days` <br>
•	**Get a speceific activity**: `{base_url}/days/{id}` (Replace {id} with the number associated with day of the week you'd like to view.

## Search for a day of the week

Searching for the day of the week in the service requires that you use the `GET` method to receive the details of the [`days`](../api/days.md) resource in the service.

To receive details of a specified activity:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/fitness-friends/api
    json-server -w fitness-tracking-db-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{{base_url}}/days/{id}`

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the id should be the same as you used in your **URL** as `{activity_id}`.
