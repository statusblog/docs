---
sidebar_position: 2
---

# Create or update a component

Components represent each part of your service or infrastructure. They are used to make it clear which parts of your service are down when an incident occurs.

## Create a component

1. Go to the **Components** tab of the [admin dashboard](../get-started/admin-dashboard.md).
2. Click **Create component** in the top right.
3. Fill out the properties of the component, then click **Save** to confirm your changes.

## Update a component

1. Go to the **Components** tab of the [admin dashboard](../get-started/admin-dashboard.md).
2. Click **Edit** next to the relevant component.
3. Change the properties of the component, then click **Save** to confirm your changes.

## Component properties

When creating or updating a component there are a variety of different properties you can change.

### Name

The name of the component. This shows up in incident communications and also on the front of your status blog.

### Status

The status of the component. You can learn more about what each one represents in our [documentation](./what-is-a-component.md).

### Description

Describes what the component represents or does. This is added as a tooltip next to the component on the status blog index.

### Display uptime

This determines whether the component publically [displays its uptime](./display-historical-uptime.md).

### Start date

This is when the component first went "live". It is used to calculate the [uptime of the component](./display-historical-uptime.md), which is displayed publically on the status blog.
