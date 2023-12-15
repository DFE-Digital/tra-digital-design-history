---
title: Recording a change history
date: 2023-12-15
description: Recording changes that are made to mandatory qualifications and making them available in an audit log.
screenshots:
  items:
    - text: Change history timeline
      src: mq-change-history.png
---

In the old Microsoft Dynamics system, there was an unstructured tab of notes attached to a record. Users would add text to explain context for changes made or extra information about something on the record.

Some records are around 20 years old and can have a lot of content attached which isn’t always needed.

However, the service do use some of the information for quality control and auditing. It can also help to answer enquiries or complaints, for example if a teacher contacts the TRA about something that was changed on their record a long time ago.

We decided to introduce this feature in the new TRS system on a case by case basis to make sure it is used only where needed and given structure. This will help to avoid bloat in the new system and make it easier to audit.

We added some questions to the action to delete a mandatory qualification, where the user can input the reason for deleting something. This creates an event which stores the user name, date and time and a code to say they deleted something. 

We decided to add the reason for deleting data to this event, as well as any evidence they uploaded such as a screenshot of an email, and a record of the data that was deleted. 

This is stored in an audit log, which we’ve called a change history.

## Change history

We used a [timeline component](https://design-patterns.service.justice.gov.uk/components/timeline/) so that the events are displayed in a logical order with the most recent first. This makes it easier to find something historic, and gives a sense of how a record has changed over time.

Currently, there are three types of event for:
- adding an MQ
- editing an MQ
- deleting an MQ

We will need to add more in future as we build more features.

The event for adding an MQ just features the core detail of the action that was taken, who did it and when. We do not need to add a reason or record of changed data because the record will contain the current data.

Editing an MQ can also include the summary which the user will have seen on the confirmation screen when making a change. If we ask for it, this shows the reason for making a change, and the old data that was being changed. This is kept in the change history so that mistakes can be resolved. It doesn’t show the new data that was being added, as this will be in the record.

Deleting an MQ also includes evidence for the change if it was uploaded. This can be used for auditing.