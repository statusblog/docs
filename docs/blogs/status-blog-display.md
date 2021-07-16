---
sidebar_position: 5
---

# Status blog display

Your public status blog index page can be reachable at any time by clicking on the **View status blog** link on the [admin dashboard](../get-started/statusblog-dashboard.md).

Here is an example status blog index page:

![status blog display](/img/status-blog-display.png)

### Name

At the top left is "My Other Service", the name of the status blog. This is configured via the **Name** field in the [blog settings](./change-blog-settings.md) in the admin dashboard.

### Subscribe button

At the top right is the subscribe button. Users can click this to subscribe to your status blog.

### Top-level status

The top level status for our example is "All Systems Operational". 

If there is an active incident, that will display here instead of the top-level status.

Otherwise, the top-level status is calculated as follows:

* If any components have **Major outage** status, it will be "Major Service Outage".
* Else if any components have **Minor outage** status, it will be "Minor Service Outage".
* Else if any components have **Degraded performance** status, it will be "Partially Degraded Service".
* Else it will be "All Systems Operational"

### Components

The components show after the top-level status. They will will display their uptime, as in this example, if they [are opted in](../components/display-historical-component-uptime.md) to do so.

### Incident history

At the bottom of the blog index page will be any recent incidents and all of their associated update, grouped by the day when the incident was created. 

