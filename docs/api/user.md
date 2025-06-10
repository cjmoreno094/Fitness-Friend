---
layout: page
---

# `user` resource

Base endpoint:

```shell

{server_url}/users
```

Contains information about the users of the service.

A user resource describes the type of the activity in the service.
Before you can create an `activity` resource in the service,
you must create the 'user' resource to assign to the `activity`.

Learn more about the [task resource](activity.md).

## Resource properties

Sample `logActivity` resource

```js

{
    "userId": "12345",
    "activity": {
      "activityId": "abc123",
      "type": "running",
      "durationMinutes": 30,
      "distanceKm": 5,
      "caloriesBurned": 300,
      "startTime": "2023-10-10T07:30:00Z",
      "endTime": "2023-10-10T08:00:00Z",
      "location": {
        "latitude": 40.712776,
        "longitude": -74.005974
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `userId` | string | The user's identification number |

## Read operations

* [Get all users](users-get-all-users.md)
* [Get users by ID](users-get-user-by-id.md)

## Create operations

* [Post users](users-post-users.md)

## Delete operations

* [Delete user by ID](Ref_DELETE_User.md)
