---
title: "System"
date: 2020-04-18T10:07:21+06:00
# post image
image: "images/blog/post-1.jpg"
# post type (regular/featured)
type: "featured"
# meta description
description: "This is meta description"
# post draft
draft: false
---


The current coronavirus pandemic has shown us just how important spaces such as libraries and offices are, but also how important and difficult it is to keep them clean and safe. ClyDe is an autonomous surface-cleaning robot meant to be deployed in these highly-trafficked spaces. It disinfects desks after they have been used, making them safe. This will assist cleaner's jobs by helping with a monotonous and repetitive task, allowing them to spend their time elsewhere.

## What can ClyDe do?

<center><img src="../media/clydepicture.png" height="500"/></center>

---

### **Surface Disinfecting**

ClyDe's main function is to autonomously clean and disinfect desk surfaces. The main target environment for ClyDe to work in are libraries, however, he could also be set to work in office spaces if desired with no modification.

ClyDe navigates throughout the environment and disinfects the surface of any desks that are marked as dirty on the accompanying database. In order to mark desks as dirty, people are asked to scan the QR code on the table using the ClyDe Companion App as they leave.

ClyDe will move to a target desk and scan the QR code on that desk in order to confirm it is the correct one. ClyDe then uses his arm which has a squeegee utensil with a sponge on the end to clean the desk. Disinfectant is absorbed into the sponge using a pump and is then spread over the table using ClyDe's cleaning arm.

ClyDe is easy to work with and maintain, all that is required after deployment is to keep the battery charged and keep the reservoir of disinfectant full.

## How does this system come into contact with users?

---

### **ClyDe Companion App**

The main way users interact with ClyDe is through our ClyDe Companion app.

<center><img src="../media/app_home.png" height="500"/></center>


#### Features

Users are only concerned with two features from the app.

The first is scanning the QR code on the table when they arrive and start using it. Since the QR code will contain the ID of the table, this allows the user to verify they are at the right table if they have booked it. This serves to let ClyDe know that the table is currently being used.

The second feature is to again scan the QR code, but this time once they have finished using the table and are leaving. This serves to let ClyDe know that the table needs to be cleaned.

It is possible in the future to integrate the app with the booking system that a library might already have in place - for instance SeatEd which is used at Edinburgh University's Main Library - allowing for a more smooth user experience.

### **ClyDe Controller**
This serves as a controller for staff to interact will ClyDe in various ways, such as telling him to start patrolling as well as to come back home.

<center><img src="../media/raspi.png" width="500" /></center>

#### Features

The controller displays information about ClyDe's status. This includes:
- Battery Level
- Reservoir Level
- Current Location
- Operation Log

See the image below for a demonstration of the UI:

![](../media/controller_ui.png)

The controller can also be used to give instructions to ClyDe. These instructions are kept simple in order to keep ease of use high. The instructions include:
- Start cleaning - this sets ClyDe off to begin patrolling and cleaning any desks that are marked as dirty.
- Return home - this prompts ClyDe to return to his home position, whether it be to allow you to charge the battery, refill the reservoir or simply to turn him off.
- Restart ClyDe - this restarts the system. In the case that there are technical issues, all you have to do is bring ClyDe to his home position and hit this button to reboot it all.
{{< youtube JvrAZXzs0NY&t=2s>
