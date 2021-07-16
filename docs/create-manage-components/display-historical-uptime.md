---
sidebar_position: 3
---

# Display historical uptime

Uptime is the percentage calculation of how something is "up" or otherwise functioning. This feature is opt-in per component. It is enabled by checking **Display uptime** when creating or updating your component.

Showcasing historical uptime helps build trust with your users, showing them how often things are fully functional within your service.

## What is looks like

The historical uptime is shown on the public facing status blog. It consists of a series of colored bars, one for each day. Additionally, it shows the total uptime calculation for the component underneath the bars.

![component uptime](/img/component-uptime.png)

If you hover your cursor over any of the bars, you can see the information for the day. 

## How it works

The uptime is a driven by **component statuses** and the **start date** for the component.

Statusblog records how long a component is in each of the given statuses (TODO). We then take that data to determine the uptime for each given day and the overall uptime. 

The start date is used to determine from which date to do this calculation. Any day that is before the start date is treated as a day with "no data". All days between the start date and when the actual component was created is treated as a day with **Operational** status.

### Day coloring

Each day is colored according the "worst" status it had on that given day. It is colored gray for days where there is no uptime data (days before the **start date**). The logic for determining the day color is as follows:

* If any seconds of **Major outage** the day is colored red.
* Else if there are any seconds of **Minor outage** the day is colored orange.
* Else if there are any seconds of **Degraded performance** the day is colored yellow.
* Else if the there are any seconds of **Operational** or **Under maintenance** the day is colored green.
* Else there is no data, and the day is colored gray.

### Uptime calculation

The uptime calculation for each component is from the following formula:

```
(total_active_seconds - outage_seconds) / total_active_seconds
```

The `total_active_seconds` is more or less the number of seconds for the given time period. It does not include any days that are "no data" (days before the **start date**).

The `outage_seconds` is computed as follows:

```
major_outage_seconds + (minor_outage_seconds * 0.3)
```

That is, each minor outage counts for 30% of an outage second. This is to reflect that a minor outage is not a full outage.


