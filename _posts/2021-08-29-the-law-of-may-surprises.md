---
layout: post 
title:  "2021-08-29 The Law of Many Surprises"
tags: [design]
---

There is a concept in software called the '[Principle of Least Surprise](https://en.m.wikipedia.org/wiki/Principle_of_least_astonishment)' which essentially states that good design should not (negatively) surprise the user. Delight the user, certainly. But as many behaviours as possible should be *expected* to the point that they're not even noticed.

Unfortunately, the reality of much software is that it runs counter to this. Perhaps this is not, in itself, unexpected. Increasing complexity of two software packages means that it is increasingly likely that they will not work perfectly together.

As a software developer - I understand this, and I empathise with the people trying to make it work. As an end-user - this makes me angry, frustrated, and sad.

## Example Google Calendars / anything else integration.

Google Calendars (currently) have four types of events:  
 1. Goal
 2. Reminder
 3. Task
 4. Event
 
Fantastical looks like a nicer calendar app than Google Calendars (and can do some neat view stuff that Google Calendars can't) ... so I'm giving it a try.

But where have my reminders gone? Oops! It looks like Google doesn't expose "reminders" and Fantastical can't see them, or create new ones. That's a bit of a pain when they've been input to ... uh ... remind me about things I'm likely to forget. And now they're all hidden from view.

After a fair bit of hunting around, it looks like Mac and Google just don't like syncing 'reminder' type events. Fantastical and Mac will sync reminder events, but that isn't enough to work for me.

So ... I can move all of my "reminders" in Google into a a new dedicated 'reminder' calendar and lose the nice checkbox/all-day representation from GCal, but at least see them in Fantastical. Okay, whatever.

Moving on ... let's look at tasks. These seem to 'just work' between Fantastical and Google Calendar. Hooray

How about getting OmniFocus items to sync across to google? Note that OmniFocus 'tasks' are not Google Calendar 'tasks' - I'll call them 'items' to try and keep that distinction. OmniFocus / Google sync seems to be a different sort of fight entirely. My ongoing effort to use Omnifocus and adopt some sort of 'GTD' system means that I'd really love OmniFocus Items with dates to sync to Google Calendar in a bi-directional way. I'm not alone in wanting this: [omnigroup forum](https://discourse.omnigroup.com/t/sync-to-google-calendar/10361/14). 
 
 So, where do we end up? I'm going to keep trying to use OmniFocs for organisation (sunk cost fallacy at work there) and Google Calendar for events that have a time ... and 'tasks' for to-do items that need to go into the calendar on specific days. 
 
 Example:
 * someone's birthday -> calendar event
 * broadband renewal date -> 'tasks' with a due date (created in Fantastical, visible in Google Calendar also)
 * plan a family get-together -> OmniFocus item(s) with no 'hard' deadline
 