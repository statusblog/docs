---
sidebar_position: 2
---

# What is Statusblog?

Statusblog is a communication tool that helps you inform your users about outages and incidents. It does this via a public facing status blog that your users can navigate to to view the current status. There they can subscribe to updates via email, getting notified whenever there is a new incident or an update to an existing incident.

## Why use Statusblog?

Statusblog is meant to serve as the communication hub for your incident management process. By enabling a transparent and praoctive incident communication process for your service, it allows you to:

* Build trust with your users and customers
* Reduce incoming support inquiries during outages
* Streamline your incident communication process

## Concepts overview

### Accounts and blogs

When you register for an account, you create a blog that is part of your account. Each account can have multiple blogs associated with it. Each blog is completely separate and have separate billing subscriptions.

Each blog you create is publically viewable by anyone with an internet connection.

### Components

Components are the various parts of your service and infrastructure. Each component has its own status that represents its current state. For example, Statusblog could be said to consist of the "admin dashboard" where you manage your blog, and the "hosted public blogs" that your users interact with, among various other components.

Component statuses are commonly when creating or updated incidents, but they can also be changed independently.

#### Component statuses:

* Operational
* Partial Outage
* Degraded Performance
* Major Outage
* Under Maintenance

### Incidents

Incidents are at the core of Statusblog. They represent any events that have occured in your service that you want to communicate to your users. Once an incident is created, it is assigned a status and a message. From there, you can send additional incident updates and change the incident status as you handle the incident.  An incident is considered done or complete once it moves to the Resolved status.

#### Incident statuses:

* Investigating
* Identified
* Monitoring
* Resolved

### Subscribers and notifications

In addition to viewing your public facing status blog to get current or historical status information of your service, users can additionally subscribe to updates via email to get notified when incidents are created, updated, or resolved.
