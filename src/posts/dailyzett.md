---
authors: ["Jan Ujcic"]
categories: ["projects"]
description: "A short DailyEmail project overview."
tags: ["daily-mail", "python", "aws"]
title: "DailyEmail"
---

## Overview

The DailyEmail is a small project designed to show how something simple can create real value. It's a mechanism that sends you an email every day with a random note from your collection. This serves as a reminder, idea generator, or just a way to revisit some long-forgotten but useful notes and ideas. I call my version the DailyZett because it sends a note from my [Zettelkasten](https://zettelkasten.de/introduction/) every morning.

## Technical details

I created the DailyZett a few years ago to get more value out of my Zettelkasten collection. While its main strength lies in the interconnections between notes, I wanted an occasional nudge to refresh my memory on topics I noted down. 

The project is essentialy a Python script that does:
1. Fetches a random note from Google Drive
3. Processes the note
4. Creates and sends an email with the note

It's that simple. The code runs on a serverless AWS Lambda function which is free for small-scale use. A CloudWatch Events Rule triggers the Lambda every morning. I chose Google Drive for storage because it's easy to update and manage my notes. Emails are sent via SMTP though I’m working on replacing this with a more secure option.

I've been using the DailyZett for years now and recently I've added a feature that prevents notes from repeating too much. A note can only reappear after a specified period. Additionally, the recipients can be added more easily with a simple config stored in the Google Drive.

You can find the Python on my Github: https://github.com/janujcic/daily-mail

## Value 

Receiving a random note every day has been very valuable for me. I helps me remember important takeaways, sparks new ideas for my daily life, and it nudges me to explore the related items in my Zettelkasten. It reduces the friction to go through your notes and triggers the creation of new ones based on your current life/work context. Often a note brought up in a random context later on has completely different meaning and relevance than it did initially. I also often create new notes based on the ideas that pop-up when reading it. 

Over time, I've added others to the recipient list and they also enjoyed it. The notes are mostly my ideas and thoughts but they bring some interesting perspectives for them too. In the future I plan be more selective about which notes to share and which ones need more refinement.

## Other uses

I adapted the same mechanism to send daily emails with selected photos as a personalized gift. As one gift, I organized photos by day with a small personalized note for that day and uploaded them to Google Drive. The Python script then retrieves the photos and a small personalized note each day and emails it to the recipient. This makes for a thoughtful gift that revives shared memories and delivers some motivation and nice thoughts to their morning. This isn't a gift for everyone but for that special person it really does make a difference because it is personalized, it requires effort to set up in a thoughtful manner, and can have a completely custom duration.

## Conclusion

I think the DailyZett or DailyEmail is a great little project offers surprising amount of value if you have a relatively big collection of notes and ideas. While there are apps that can do this in a fraction of this time, this project gives you full control and customization. Plus, building it teaches you some useful things in AWS and Python.

In the future, I might make a complete guide for this because it is a great way to learn some new skills while also creating a useful mechanism for sending emails to you or your closed-ones. 