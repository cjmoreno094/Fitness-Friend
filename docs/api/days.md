# `days` resource

Base endpoint:

```shell
{server_url}/days
```

Contains information about the days of the week of the service.

The days of the week resource describes the type of the activity in the service.
Before you can create an `activity` resource in the service,
you must edit the 'days' resource and assign and `activity` to it.

Learn more about the [activities resource](activities.md).

### Resource properties

Sample `days` resource

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

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `day` | string | The day of the week |
| `activity` | string | Notifies the user if they're working out that day. Will include either a `Y` to indicate Yes, or an `N` to indicate No |
| `activity_id"` | number | The unique record ID associated with the activity scheduled for that day|
| `id` | number | The unique record ID associated with the day of the week, beginning numerically with `1` as Monday |

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

### Read

* [Get activities assigned to the days of the week](./get-days.md)


## See Also

### Overview

* [Head back to the homepage](../index.md)

### Resources

* [Activities resources](./activities.md)
* [Days resources](./days.md)

### Read

* [Get all activities](./get-activities.md)

### Create

* [Add an activity resource](./post-new-activity.md)

### Edit

* [Edit a day of the week](./put-days.md)

### Delete

* [Delete an activity](./delete-activities.md)