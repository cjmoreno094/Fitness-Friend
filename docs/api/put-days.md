# Put a day of the week

In this tutorial, you learn the endpoints to `PUT` 
a day of the week in the service.

## URL

```shell
{server_url}/days/{id}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `user_id` | number | The ID of the user resource assigned to this task |
| `title` | string | The title or short description of the task |
| `description` | string | The long description of the task |
| `due_date` | string | The [`ISO 8601`](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due |
| `warning` | number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`. |
| `id` | number | The task's unique record ID |

## Request headers

`Content-Type: application/json`

## Request body

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
| 200 | Success | Requested data updated successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |


After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.

## Next Steps

### Resources

* [Activities resources](./activities.md)

## See Also

### Overview

* [Head back to the homepage](../index.md)

### Resources

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