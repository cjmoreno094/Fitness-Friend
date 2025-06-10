---
layout: page
---

# `activity` resource

Base endpoint:

```shell

{server_url}/activity
```

Contains information about tasks stored for the users of the service.

To have a task in the service, the user must be added to
the service first. Learn more about the [user resource](user.md).

## Resource properties

Sample `activity` resource

```js

{
    "activityId": "abc123",
    "type": "running",
    "date": "2023-10-10",
    "durationMinutes": 30,
    "distanceKm": 5
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `activityId` | number | The ID of the activity reference to which this activity is assigned |
| `type` | string | The name of the activity |
| `date` | string | The date you completed this activity |
| `durationMinutes` | number | The time it took to complete this activity |
| `distanceKM` | number | The distance relative to the `durationMinutes` that the activity took to complete. This should be in kilometeres (KM).

## Read

* [Get all tasks _(coming soon)_](#resource-properties)
* [Get task by ID _(coming soon)_](#resource-properties)
* [Get task by user ID](./tasks-get-tasks-by-user-id.md)
* [get task with full-text search](./tasks-get-tasks-with-search)

## Create

* [Add a task resource](./tasks-add-a-task.md)

## Update

* [Put task by ID](./tasks-put-task-by-id.md)
