# Delete an activity

In this tutorial, you learn the endpoints to `DELETE` 
an activity in the service.

## Before you start

Make sure you've completed read the [get started guide](before-you-get-started.md) topic on the development system you'll use for the tutorial.

## What method are we using?

`PUT`

## What endpoints are we using?

- Delete an activity: {base_url}/delete/activity/{activity_id}

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `activity_id` | number | The record `id` of the activity to delete |


### Return body

```js
{}
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

### Resources

* [Days resources](./days.md)


## See Also

### Overview

* [Head back to the homepage](../index.md)

### Resources

* [Activities resources](./activities.md)

### Read

* [Get all activities](./get-activities.md)
* [Get activities assigned to the days of the week](./get-days.md)

### Create

* [Add an activity resource](./post-new-activity.md)

### Edit

* [Edit a day of the week](./put-days.md)

### Delete

* [Delete an activity](./delete-activities.md)