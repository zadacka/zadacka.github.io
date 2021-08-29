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

Okay ... so let's How about getting OmniFocus items to sync across to google? Note that OmniFocus 'tasks' are not Google Calendar 'tasks' - I'll call them 'items' to try and keep that distinction. OmniFocus / Google sync seems to be a different sort of fight entirely. My ongoing effort to use Omnifocus and adopt some sort of 'GTD' system means that I'd really love OmniFocus Items with dates to sync to Google Calendar in a bi-directional way. I'm not alone in wanting this: [omnigroup forum](https://discourse.omnigroup.com/t/sync-to-google-calendar/10361/14). Being able to see OmniFocus items (when they have due dates / times populated) on a calendar seems like a natrual idea. Some [macpowerusers.com users agree](https://talk.macpowerusers.com/t/is-there-a-calendar-app-that-also-displays-omnifocus-tasks/22435/2).
 
 So, where do we end up? I'm going to keep trying to use OmniFocs for organisation (sunk cost fallacy at work there) and Google Calendar for events that have a time ... and 'tasks' for to-do items that need to go into the calendar on specific days. 
 
 Example:
 * someone's birthday -> calendar event
 * broadband renewal date -> 'tasks' with a due date (created in Fantastical, visible in Google Calendar also)
 * plan a family get-together -> OmniFocus item(s) with no 'hard' deadline
 
 So ... *Forget reminders. Reminders are now dead to me.* Long live Tasks. Goals are YAGNI for me right now. Ignore Goals too. OmniFocus items will need to be manually sync'ed to some form of calendar thing if/when I get there. 
 
 # Google Calendar Default ... What The Fudge?
 
Google apparently likes to use the Principle of Most Surprise.
* Google Calendar (used via Chrome) shows my calendar called 'Vacation'
* Google Calendar (iOS App) shows my 'Vacation' calendar as 'Events'

The default calendar is *always* 'Vacation'. It cannot be changed. Ever. Advice online about 'your default calendar is the last one that you used' is no longer correct. Current best advice is to export / rename / import in order to switch 'default' calendar (source: [calendar.com](https://www.calendar.com/blog/how-do-i-change-my-default-calendar-in-google-calendar/)). 

Like ... seriously guys? If you wanted to chnage a lightbulb, could you really believe that the best way to do so would be to KNOCK DOWN THE WHOLE HOUSE, move to somewhere with a working light bulb, and then re-build the house around it? 

Two major issues here:
1. This stuff is *so hidden*. The calendar names are different in different Google Apps (via Chrome and via iOS). The 'Events' name is kinda more true to the special nature of the Default calendar. So call it Default everywhere! And have a clear line of text in the settings saying that you can't change the default!!
2. The ability to change default calendar seems really, really, basic. And it used to be there, and it went away. 

Anyhow. Surprise! That's another hour of my life that I'm not gonna get back. Whenever the next person at work asks how we can learn to run the company 'more like google', I'm gonna have to smile and try really hard TO SCREAM ONLY INSIDE MY HEAD and not out loud.