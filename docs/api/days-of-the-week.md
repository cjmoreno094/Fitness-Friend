---
layout: page
---

# `days_of_the_week` resource

Base endpoint:

```shell

{server_url}/days_of_the_week
```

Contains information about the days of the week of the service.

The days of the week resource describes the type of the activity in the service.
Before you can create an `activity` resource in the service,
you must create the 'days-of-the-week' resource to assign to the `activity`.

Learn more about the [activities resource](activities.md).

## Resource properties

Sample `days-of-the-week` resource

```js

{
    "Monday": [
        {
            "activity": "Y",
            "userId": 1
}

```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `activity` | string | Notifies the user if they're working out that day. Will include either a `Y` to indicate Yes, or `N` to indicate No |
| `userId` | number | The task's unique record ID |

## Read operations

## Create operations

* [Post users](users-post-users.md)

## Delete operations

* [Delete user by ID](Ref_DELETE_User.md)
