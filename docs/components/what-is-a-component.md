---
sidebar_position: 1
---

# What is a component?

A component a part of your service and infrastructure. Each component has its own status that represents its current state. For example, Statusblog could be said to consist of the "admin dashboard" where you manage your blog, and the "hosted public blogs" that your users interact with, among various other components.

## Component statuses

Each component has an associated status that represents the current state of the component:

* Operational
* Under maintenance
* Degraded performance
* Partial outage
* Major outage

### Operational

The component is operating as normal. This is the status it will be in the vast majority of the time.

### Under maintenance

The component is currently under maintenance. 

### Degraded performance.

The component is slow or not functioning in some minor way. For example, a component slowing down under significantly larger-than-usual traffic.

### Partial outage

The component is completely broken for some users, or for some specific use cases that not all depend on.

### Major outage

The component is completely broken and unavailable for all users.

## Changing component status

The component status is typically managed when creating or updating an incident (TODO). However, it can also be changed indepepntly of any incident:

1. Go to the **Components** tab in the [admin dashboard](../get-started/statusblog-dashboard.md).
2. Click **Edit** on the relevant component.
3. Change it in the **Status** dropdown.
4. Click **Save** in the bottom right to save your change.

