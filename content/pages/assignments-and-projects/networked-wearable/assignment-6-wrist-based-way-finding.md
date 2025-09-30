---
content_type: page
description: This page presents a student group's work on Assignment 6 (Networked
  Wearable) - the wrist-based way-finder.
learning_resource_types:
- Assignments
ocw_type: CourseSection
parent_title: 'Assignment 6: Networked Wearable'
parent_type: CourseSection
parent_uid: 202ac8dd-885c-dd02-7531-38f0e50235da
title: 'Assignment 6: Wrist-based Way-finding'
uid: 77520b74-548a-605c-22bd-5f4919a9b598
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---

{{< tableopen >}}
{{< tropen >}}
{{< tdopen >}}
« Previous: Return to {{% resource_link 202ac8dd-885c-dd02-7531-38f0e50235da "Assignment 6 description" %}}
{{< tdclose >}}
{{< tdopen >}}
Next: {{% resource_link d9c64252-0aba-741e-8bc3-ef40039896ca "student work sample" %}} »
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}

_New Textiles students: Dawn Wendell, Rizal Muslimin and anonymous student  
Communicating with Mobile Technologies students: Thomas Lipoma and anonymous MIT student_

{{< resource "5ea4e4df-6097-8246-e772-bd5f8764009a" >}}

The wristband component of the way-finder.

For our collaboration with the Communicating with Mobile Technologies class, we decided to make a wearable information display with two RGB LEDs. We envisioned these LEDs being used for guidance similar to the kids games of "simon says" or "hot and cold", with the LEDs changing colors in response to the user's orientation and distance from a target location. This is a more passive way of giving directions, with the user having to be actively involved in the discovery of the target place.

The Textiles team built a wrist-based device, connected with the LilyPad and two RGB LEDs. We also completed the bluetooth connection from the phone to the device and troubleshot the system using the output from the phone compass.

{{< resource "fc050869-284c-bde4-ddac-dd324311bbe5" >}}

Design elements of the wrist-based way-finder.

{{< resource f5c486c5-e4c8-0ee9-8e26-e334108af764 >}}

Here is a video of the wristband responding to compass directions from the phone.

One LED changes color in response to the orientation of the phone, and the other LED changes from red to green when the phone has been held in the green ("correct") position for longer than 3 seconds. This pause / response is intended to signify that you have traveled in the correct direction and have now arrived at the destination.

{{< resource "3303bca9-c908-aae5-9d92-faa119bcacff" >}}

Potential applications include mobile navigation support and physiological monitoring. (Map image source © Google. All rights reserved. This content is excluded from our CreativeCommons license. For more information, see [http://ocw.mit.edu/fairuse](/fairuse))

Lessons Learned
---------------

*   We tried to make our own circuit, but were not able to get it working. Should have tested the circuit before sewing it to the wristband.
*   The battery holder we were given gave us lots of trouble - the leads kept falling off so we spent a lot of time ripping them off the wristband and resoldering them, even though we tried to sew the leads in place for strain-relief.
*   It was very hard to do anything in parallel because we had one device, one LilyPad, one phone, and two groups from the Mobile Technologies class who both needed to use the textile device.
*   Scheduling undergrads and grads together is HARD. We were never able to actually meet up with our Mobile Technologies teammates.

{{< resource "da978b68-063b-3791-e737-906aed8fd3cb" >}}

Testing the system.

Contributions
-------------

Anonymous student: software, phone connection  
Dawn: wristband, documentation  
Rizal: circuit, soldering, documentation

Code
----

BDR Standalone ({{% resource_link 931f1939-123d-ee3a-7077-2886289249b6 "TXT" %}})  
BDR Integrated ({{% resource_link 4cb0c882-10ec-3230-fcf2-35f8e2292b50 "TXT" %}})

{{< tableopen >}}
{{< tropen >}}
{{< tdopen >}}
« Previous: Return to {{% resource_link 202ac8dd-885c-dd02-7531-38f0e50235da "Assignment 6 description" %}}
{{< tdclose >}}
{{< tdopen >}}
Next: {{% resource_link d9c64252-0aba-741e-8bc3-ef40039896ca "student work sample" %}} »
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}