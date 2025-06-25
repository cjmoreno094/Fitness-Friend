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

## Resource properties

Sample `days` resource

```js

{
    "day": "Monday", 
    "activity": "Y",
    "activityId": 1,
    "id": 1

```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `day` | string | The day of the week |
| `activity` | string | Notifies the user if they're working out that day. Will include either a `Y` to indicate Yes, or an `N` to indicate No |
| `activity_id"` | number | The unique record ID associated with the activity scheduled for that day|
| `id` | number | The unique record ID associated with the day of the week, beginning numerically with `1` as Monday |

## Read operations

## Create operations

* [Post users](../api/days.md)

## Delete operations

* [Delete user by ID]()
