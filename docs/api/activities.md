# `activities` resource

Base endpoint:

```shell
{server_url}/activities
```

Contains information about activities assigned to the days of the week.

To have a activities in the service, the user must be added to
the acitivity first. Learn more about (coming soon).

## Resource properties

Sample `activities` resource

```js
[
   {
   "day_id": 1,
   "activity_type": "running",
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

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `day_id` | number | The ID of the corresponding day of the week resource to which this activity is assigned |
| `activity_type` | string | The type of activity |
| `durationMinutes` | number | The time it took to complete this activity |
| `distanceKM` | number | The distance relative to the `durationMinutes` that the activity took to complete. This should be in kilometeres (KM) |
| `caloriesBurned` | number | The amount of calories burned during the activity |
| `startTime` | number | The date and time the user started the activity |
| `endTime` | number | The date and time you completed the activity |
| `notes` | string | Any details about the activity |
| `id` | number | The activity's unique record ID |


## Next Steps

### Read

* [Get all activities](./get-activities.md)


## See Also

### Overview

* [Head back to the homepage](../index.md)

### Resources

* [Activities resources](api/activities.md)
* [Days resources](api/days.md)

### Read

* [Get activities assigned to the days of the week](./get-days.md)

### Create

* [Add an activity resource](./post-new-activity.md)

### Edit

* [Edit a day of the week](./put-days.md)

### Delete

* [Delete an activity](./delete-activities.md)
