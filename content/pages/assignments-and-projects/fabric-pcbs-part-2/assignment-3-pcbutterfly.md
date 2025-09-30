---
content_type: page
description: ''
hide_download: true
hide_download_original: null
learning_resource_types:
- Assignments
ocw_type: CourseSection
parent_title: 'Assignment 3: "Hello World" Fabric PCBs, Part 2'
parent_type: CourseSection
parent_uid: 65b98bff-a576-b7e8-689b-c6366c1e63d3
title: 'Assignment 3: PCButterfly'
uid: 1805af5b-ecab-6b00-7d48-946d9bb9cafe
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---

{{< tableopen >}}
{{< tropen >}}
{{< tdopen >}}
« Previous: {{% resource_link 5af02bea-0868-c0fa-845e-79cc65770c1e "student work sample" %}}
{{< tdclose >}}
{{< tdopen >}}
Next: Return to {{% resource_link 65b98bff-a576-b7e8-689b-c6366c1e63d3 "Assignment 3 description" %}} »
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}

_By Xiao Xiao and two anonymous MIT students_

{{< resource "faff50f7-536c-21d9-47e5-1876bd12ab58" >}}

The PCButterfly

The Concept
-----------

Our design is a light sensitive butterfly that turns on when in the dark. It can be easily incorporated onto clothing, bags, hair accessories etc. Our switch is a phototransistor located on the body of the butterfly design. Since the phototransistor is sensitive to changes in light it can be activated by shining and then removing the light source, yet will remain inactive in ambient light conditions.

The ATtiny13 microcontroller, has 4 pins available to connect to LEDs. Two allowed for pulse width modulation (PWM) so we decided to make the layout of the LEDs symmetrical with a pair that fade on and off on the upper wings, and ones that are steady on the lower wings.

The Design
----------

{{< resource "71d7505f-d718-a56b-ddb9-7bab7564e726" >}}

We first tested the layout on a breadboard before designing the actual butterfly circuit pattern.

{{< resource "c81fd30e-1f6c-2543-5a19-d63e5aa49e9c" >}}

The circuit diagram shows the phototransistor at B3, and LEDs connected at B0, B1(PWM lights) B2, B4 (non-PWM) B5 is for reset and is unconnected.

Our code ({{% resource_link 5648e55c-ddab-0a07-6686-b5734b94136b "TXT" %}})

There are two main fabric layers – a bottom layer for the main conductive area of the circuit, and the top layer that supports the ground wire, phototransistor, LEDs and resistors. The design incorporates iron-on adhesive conductive fabric as the substrate for the circuit. The phototransistor, LEDs and resistors are through components that source power through the microcontroller located at the center of the butterfly layout. A wire frame serves as an easily accessible ground wire as well as a structural support, which can be positioned to give the butterfly a more realistic shape.

{{< resource "4b6e8503-97d6-4b4b-1e1d-cc28fcf5b54d" >}}

Top view of the PCButterfly.

An overall (cutting schematic) was rendered with Adobe Illustrator. A different image layer represents each fabric. Before cutting, it is necessary to separate the layers into discrete files in a format that can be imported to the laser cutter (ai v. 7, .dmx). Silicone molds were also created to add epoxy coatings to protect the soldered connections on the underside of the structure.

{{< resource "7ca08c5f-a2fc-7fa6-e85f-cee9ce276a68" >}}

Laser cutter schematic.

This video shows the laser cutter scoring our circuit. It is important to cut with the paper side up - so you may have to make a reflection of your design.

{{< resource 9034c6e0-6225-b0a8-0898-25fc43c17a4e >}}

PCButterfly laser cutter fabrication

The Fabrics
-----------

We tested a variety of fabrics including denim, leather and lightweight lining material. We wanted to be able to incorporate a range of textures into our design and allow for easy customization by simply rearranging the materials. The lining fabric was a bit too light to use on its own reliably, although we would like to experiment more with light fabrics in the future. The laser cutter was an ideal tool for creating decorative cutout designs on the wings. Both the denim and leather provided a robust structure for our PCB and our final design included a leather underside (most of the conductive fabric was adhered to this layer), lining fabric middle layer, and a denim top layer (ground wire frame, LEDs and resistors on this side).

{{< resource "3ee901ff-ee3e-ca15-3628-33fda07b330e" >}}

Leather underside, with most of the conductive fabric.

{{< resource "5ca07f3a-b31f-bc87-bf0d-80db40e80632" >}}

The PCButterfly in action.

{{< resource ce0ab668-48ec-e60e-fdff-892ca8bc5006 >}}

Video of the PCButterfly in action.

Troubleshooting
---------------

We originally used PB5 of the AVR as the sensor pin in our prototype circuit because of location convenience. However, we got very strange behavior of the lights. It turned out that PB5 is also the reset pin, which resets the chip every time it's pulled low, which meant that every time the light turned off, the chip reset. We switched the sensor to PB3, and everything worked fine.

The day before the project was due, we were testing the chip and accidentally shorted power with ground for about 30 seconds before realizing it. Doing that killed the chip, and we were left with a butterfly with 3 LEDs that flickered erratically and wasn't responsive to light. Luckily, we had extra material and made another one. If we were to iterate on the design, we would hide the ground wire so that clipping to VCC cannot possibly touch the ground.

It is relatively easy to dislodge the soldered connections with minor manipulation. It is very useful to have a multi-meter on hand to test individual connections.

{{< tableopen >}}
{{< tropen >}}
{{< tdopen >}}
« Previous: {{% resource_link 5af02bea-0868-c0fa-845e-79cc65770c1e "student work sample" %}}
{{< tdclose >}}
{{< tdopen >}}
Next: Return to {{% resource_link 65b98bff-a576-b7e8-689b-c6366c1e63d3 "Assignment 3 description" %}} »
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}