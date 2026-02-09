---
authors: ["Jan Ujcic"]
categories: ["projects"]
description: "A short description of SNDevOps extension."
tags: ["extensions", "ServiceNow", "Azure DevOps"]
title: "SNDevOps Extension"
layout: post.html
---

## Project Overview: SNDevOps Extension

SNDevOps is a simple WYSIWYG extension that simplifies the review process of ServiceNow pull requests in Azure DevOps. Azure DevOps enables easy reviews of code changes but unfortunately, scripts form only a smart part of the files usually committed from ServiceNow. A large part of committed files are XML configuration files. Reviewing these XML files effectively often requires viewing them in the ServiceNow platform itself.

## How it works

This extension scans the Azure DevOps pull request page for key information and generates a dropdown menu for each commit. The menu provides direct links to view the corresponding file in different ServiceNow environments. This is particularly useful for reviewing low-code elements like flows, which are nearly impossible to assess properly in their raw XML format.

By allowing reviewers to quickly access and view configuration files rendered in the platform, SNDevOps extension helps us achieve faster, more accurate reviews.

## Value

- **Time savings:** files in ServiceNow can be opened with a single click, eliminating the need to manually search for them on the platform.
- **Higher quality reviews:** reducing the friction for thorough reviews makes it easier to review each commit thoroughly, rather than skipping some that seem fine at first glance.
- **Improved workflow:** quickly accessing file and returning to the pull request helps maintain focus on the overall context, results in better reviews.

## Code

You can find the source code on my [Github](https://github.com/janujcic/sn-devops-extension)
