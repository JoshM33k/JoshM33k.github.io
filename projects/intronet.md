---
layout: project
title: IntroNet - Speed Networking
description: Speed dating, but for making business contacts.  Matches participants on shared interests, then generates meeting schedules for everyone to follow.
---

IntroNet is software I developed as part my graduate software engineering course, with additonal development and features added later as a part of my work with the [Security and Software Engineering Rsearch Center (S2ERC)](http://www.serc.net/).

IntroNet is a speed networking tool that pairs participants based on common interests (think speed dating for business contacts).  The idea was developed with large conferences in mind.  Many people attending may share your same research interests or areas of study, and could provide you with a contact, resources, help with a paper, etc. but finding those people might sometimes be a challenge.

A conference can solve that problem by using IntroNet.  First, before the event, participants will fill out an online questionnaire, listing their research interests.  This online form data is saved as a csv file.  Then IntroNet parses the CSV file, reading in all the participant information, so that it may create a custom schedule for each participant, pairing them for 5-10 minutes at a time with another person interested in the same things they are.  Depending on the conference and the time permitting, any number of these meetings can be set to take place.

As it turns out, matching people up based on common interests and assigning meetings based on availability is a pretty hard problem.  IntroNet does it in a couple of passes.  The first time through, it makes as many meetings as it can based on interests alone, and then does another pass, plugging any holes in schedules as best it can (sometimes, a meeting has to be made with a random person, as no interests may be shared with anyone else).  Lots of considerations popped up along the way that weren’t initially factored in.  For example, sometimes you are left with 3 people who all need to meet with someone at a given time.  To accomodate that, IntroNet had to be able to create a group of three on the fly for those people.

Later features that were added include the ability to prearrange a meeting between two participants (so that it will always happen), and to generate partial schedules if someone can’t attend the entire event.  The ability to schedule a “Poster Parade” was also developed, which paired a number of people with a specific poster for a given amount of time, also based on their interests.

IntroNet has been used at two different S2ERC conferences in 2011-2012, each time with close to 100 people involved.