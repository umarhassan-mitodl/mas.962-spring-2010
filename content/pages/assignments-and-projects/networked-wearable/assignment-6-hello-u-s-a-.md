---
content_type: page
description: This page presents a student group's work on Assignment 6 (Networked
  Wearable).
draft: false
learning_resource_types:
- Assignments
ocw_type: CourseSection
parent_title: 'Assignment 6: Networked Wearable'
parent_type: CourseSection
parent_uid: 202ac8dd-885c-dd02-7531-38f0e50235da
title: 'Assignment 6: Hello U.S.A.!!'
uid: d9c64252-0aba-741e-8bc3-ef40039896ca
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---
{{< tableopen >}}{{< tbodyopen >}}{{< tropen >}}{{< tdopen >}}
« Previous: {{% resource_link 77520b74-548a-605c-22bd-5f4919a9b598 "student work sample" %}}
{{< tdclose >}}{{< tdopen >}}
Next: Return to {{% resource_link 202ac8dd-885c-dd02-7531-38f0e50235da "Assignment 6 description" %}} »
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}

*By Yang Yang and three anonymous MIT students*

{{< resource 29dbd6d1-6de1-31b0-6ac2-55ae6328cd2f >}}

Coordinate system that we used to light the LEDs from the LilyPad.

These Vertical pins were set to LOW: 11, 12, 13, a0(14), a1(15), a2(16), a3(17), a4(18), a5(19), 2, 3.     
These Horizontal pins were set to HIGH: 10, 9, 8, 7, 6, 5, 4.

## Charlieplex State Drawing Detail

We did not have enough pins on our LilyPad to control each led separately. Using charlieplexing we can have up to n/2\*(n/2) leds, where n is the number of pins on our Lilypad.

A grid of conductive fabric was made, positive legs of the LEDs were sewn to horizontal bars, the ground leg was sewn to the vertical strips.

We could then program the power to be sent to each LED, and turn all the others off by making them the opposite charge of the LED we wanted to light up.

The horizontal pins were set to HIGH and the vertical pins set to LOW. Each state had an associated LED, to turn on a particular pin its horizontal bar was called at HIGH and its vertical bar was called at LOW.

Wikipedia has a good reference article on [charlieplexing](http://en.wikipedia.org/wiki/Charlieplexing).

Charlieplexing

{{< resource fcfe9320-4021-0fec-9d80-9dd71c24fe43 >}}

The back of the map. The LEDs are sewn positive leg to horizontal and ground to vertical. Felt pads are used to keep horizontal and vertical layers apart.

{{< resource b9b68943-6ae3-56ca-559e-d6a4373fbd6a >}}

The LilyPad layer set over the charlieplex felt layer. This is the final layer that has the conductive thread connecting from the LilyPad to the charlieplex grid at the edges of the felt.

{{< tableopen >}}{{< tbodyopen >}}{{< tropen >}}{{< tdopen >}}
« Previous: {{% resource_link 77520b74-548a-605c-22bd-5f4919a9b598 "student work sample" %}}
{{< tdclose >}}{{< tdopen >}}
Next: Return to {{% resource_link 202ac8dd-885c-dd02-7531-38f0e50235da "Assignment 6 description" %}} »
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}