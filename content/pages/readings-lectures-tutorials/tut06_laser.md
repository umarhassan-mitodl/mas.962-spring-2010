---
content_type: page
description: Tutorial for the laser cutting portion of the course.
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: Readings, Lectures & Tutorials
parent_type: CourseSection
parent_uid: e974bd1a-9897-6b46-896a-13de54082f58
title: Laser Cutter Tutorial
uid: b8152aef-691c-0825-0ce2-97f34c7b6768
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---
{{% resource_link "e974bd1a-9897-6b46-896a-13de54082f58" "Readings, Lectures & Tutorials Index" "#ses6" %}} | {{% resource_link "4bbdee6e-bb42-6142-21cf-13f92a364c47" "AVR Programming, Part 1" %}} »

WARNING NOTICE:

The activities described on this page are potentially hazardous and require a high level of safety training, special facilities and equipment, and supervision by appropriate individuals. You bear the sole responsibility, liability, and risk for the implementation of such safety procedures and measures. MIT shall have no responsibility, liability, or risk for the content or implementation of any of the material presented. [Legal Notice](https://ocw-studio.odl.mit.edu/terms/)

We have a Bright Star LG500tt 60 Watt laser cutter.

**WARNING:** The laser cutter is a powerful, but very dangerous tool. If you use it incorrectly you can poison yourself (and others) and burn down the building. Use it carefully and thoughtfully. In particular: do NOT cut dangerous or unknown materials, and NEVER leave the machine unattended while it is cutting.

**1\. Create the pattern you are going to cut using a drawing program like Adobe Illustrator**

Note: the laser cutter software only recognizes vector lines (the paths of lines). It does not recognize filled shapes or line widths. Here's a sample file in Adobe Illustrator:

- ATtiny13FabricPCB.ai ({{% resource_link "9900d2d5-4755-6a5c-dd17-60de805b8de4" "AI" %}})

This is for a fabric PCB for the ATtiny13 microcontroller. The drawing includes components for the circuitry and the backing fabric.

{{< resource uuid="6fff9ae3-a69f-1a1b-a585-428bdb38fc14" >}}

Drawing pattern for laser cutter: circuitry and backing fabric.

**2\. Export your drawing**

The laser cutter software can import Illustrator files (version 7.0 only, .ai), HPGL files (.plt), and Drawing Exchange Format files (.dxf). To create a readable file, export your drawing in one of these formats. Save all text as curves.

**3\. Open the LaserCut 5.1 software**

**4\. Import your drawing**

Go to File→Import and select your drawing file.

Alternately, you can open an existing laser cutter file (.ecp). Here is my fabric PCB file in ecp format:

- ATtiny13FabricPCB.txt ({{% resource_link "c55ed916-8966-084f-db55-8b0f099b3e6e" "TXT" %}})

(Note: change the extension from .txt to .ecp after downloading. Wiki software does not allow you to upload and post .ecp files.)

**5\. Get your material ready**

Make sure your material is safe to cut.

**WARNING:** Do not cut anything unless you are positive it is safe!!! Cutting unsafe materials - e.g. PVC, vinyl, or that mysterious plastic you picked up in Chinatown - can cause serious damage to your health and that of those around you. Don't do it! 

Safe materials include: wood, paper, acrylic, cotton, wool, and silicone.

Unsafe materials include: vinyl, PVC, and any highly reflective material.

Make sure your material fits into the laser cutter. The high-low tech laser bed is 30cm x 50 cm, approximately 12 x 20 inches.

**6\. Find the proper settings for your material and position your drawing in the software**

Choose the appropriate settings for different materials. Note: you can match different colors to different cut/engrave settings within one drawing. The order in which the colors are listed in the software is the order in which they will be cut.

**7\. Save your .ecp file if you want the layout & cut settings for your drawing saved**

**8\. Turn everything on and home the machine.**

Turn on the power strip that's to the right of the machine. This turns on the laser cutter, air filter, and cooling system. When everything is on, it's loud!

{{< resource uuid="8ae8fbaa-57b8-8be6-88d6-9ffbc9c04bdd" >}}

Power strip for the laser cutter, air filter, and cooling system.

Press the reset button on the machine controls or in the software to home the machine. Note: not homing the machine will result in the machine attempting to cut beyond its boundaries. It's an important step!

{{< resource uuid="55d24872-e03b-7f7f-fc0d-7c25d525db3a" >}}

The laser cutter control panel.

**9\. Focus the laser cutter**

**WARNING:** The risk of fire drastically increases when the laser cutter is not focused properly.

Place your material into the machine.

Use the arrow keys on the machine controls or in the software to move the laser head over your material.

Get the focusing tool, which is magnetically attached to the front of the machine.

{{< resource uuid="7c307214-3b41-1214-cbde-78c08dd1d73d" >}}

The focusing tool, attached to the front of the laser cutter.

Use the focusing tool and the socket wrench to adjust the height of the bed so that the notch on the focusing tool rests on the plate that is holding the lens. This will focus the laser at the surface of your material.

{{< resource uuid="2c0c390a-69eb-ff9d-40a3-6b19680932d8" >}}

Adjusting the height of the bed.

Adjusting the height of the table:

{{< resource uuid="37bb1e66-db61-aefc-01a6-25424d994d80" >}}

Adjusting the height of the table.

When you're done focusing, return the focusing tool to the front of the machine and the socket wrench to the platform inside the machine.

**10\. Cut your part**

**WARNING:** Never leave a running job unattended. You can very easily burn down the building!

To test the boundaries of your cut job, hit the edge button on the machine controls or in the software. This will move the laser cutter head in a square around the perimeter of your job. This is a good way to determine if your drawing and material are properly aligned.

- Hit start to begin the job.
- Hit pause to pause the job. Hitting start again will resume the job.
- Hit stop to stop the job. Hitting start again after you've pressed stop will start the job from the beginning. You can also open the lid of the laser cutter to immediately stop cutting.
- Hitting the big red STOP safety button will immediately turn off the machine.

{{% resource_link "e974bd1a-9897-6b46-896a-13de54082f58" "Readings, Lectures & Tutorials Index" "#ses6" %}} | {{% resource_link "4bbdee6e-bb42-6142-21cf-13f92a364c47" "AVR Programming, Part 1" %}} »