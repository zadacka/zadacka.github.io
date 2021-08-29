---
layout: post 
title:  "2021-08-29 The Law of Many Surprises"
tags: [design]
---

There is a concept in software called the '[Principle of Least Surprise](https://en.m.wikipedia.org/wiki/Principle_of_least_astonishment)' which states that good design should not surprise the user. As many behaviours as possible should be *expected* to the point that they're not even noticed. 

Unfortunately this principle is often violated. Increasing complexity of any two software packages will increase the likelihood that they will not work perfectly together. As things grow apart it is unsurprising that they may stop working together as nicely as they once did.

*As a software developer* I understand this and empathise with fellow developers working on either project. *As an end-user* it makes me angry, frustrated, and sad when things don't "just work", especially when it seems reasonable that they should (or they used to in the past).

## Example Google Calendars / anything else integration.

Google Calendars (currently) have four types of thing:  
 1. Goal
 2. Reminder
 3. Task
 4. Event
 
Fantastical looks like a nicer calendar app than Google Calendars (and can do some neat view stuff that Google Calendars can't) ... so I'm giving it a try.

But where have my reminders gone? Oops! It looks like Google doesn't expose "reminders" and Fantastical can't see them, or create new ones. That's a bit of a pain when they've been input to ... uh ... remind me about things I'm likely to forget. And now they're all hidden from view.

The real issue here is that the four types of Google Calendar thing have specific meanings within the Google world that don't map perfectly to other systems ... and then this is made worse by restrictive APIs by Google and Apple that make it hard for third party developers to implement any 'best effort' thing on top. 

Reminders vs Tasks vs Events: [google.support forum](https://support.google.com/calendar/thread/3263294/what-is-the-difference-between-events-reminders-and-tasks?hl=en)

After a fair bit of hunting around, it looks like Mac and Google just don't like syncing 'reminder' type events. Fantastical and Mac will sync reminder events, but that isn't enough to work for me.

Let's look at tasks. These seem to 'just work' between Fantastical and Google Calendar. Hooray! They can take a date and they are reasonably visible. They can be marked as 'done'. Basically ... tasks seem to be a superset of everything that I wanted reminders to do. If I lived in the Android ecosystem I might care about the ability to create Reminders from voice commands / see them in some 'reminders' app that doesn't play nice with Tasks. But that ain't me.

Okay ... so let's How about getting OmniFocus items to sync across to google? Note that OmniFocus 'tasks' are not Google Calendar 'tasks' - I'll call them 'items' to try and keep that distinction. OmniFocus / Google sync seems to be a different sort of fight entirely. My ongoing effort to use Omnifocus and adopt some sort of 'GTD' system means that I'd really love OmniFocus Items with dates to sync to Google Calendar in a bi-directional way. I'm not alone in wanting this: [omnigroup forum](https://discourse.omnigroup.com/t/sync-to-google-calendar/10361/14). 
 
 So, where do we end up? I'm going to keep trying to use OmniFocs for organisation (sunk cost fallacy at work there) and Google Calendar for events that have a time ... and 'tasks' for to-do items that need to go into the calendar on specific days. 
 
 Example:
 * someone's birthday -> calendar event
 * broadband renewal date -> 'tasks' with a due date (created in Fantastical, visible in Google Calendar also)
 * plan a family get-together -> OmniFocus item(s) with no 'hard' deadline
 
 So ... *Forget reminders. Reminders are now dead to me.* Long live Tasks. Goals are YAGNI for me right now. Ignore Goals too. OmniFocus items will need to be manually sync'ed to some form of calendar thing if/when I get there. 