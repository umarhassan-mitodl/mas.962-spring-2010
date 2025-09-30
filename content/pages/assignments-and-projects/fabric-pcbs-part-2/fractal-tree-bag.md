---
content_type: page
description: ''
draft: false
learning_resource_types:
- Assignments
ocw_type: CourseSection
parent_title: 'Assignment 3: "Hello World" Fabric PCBs, Part 2'
parent_type: CourseSection
parent_uid: 65b98bff-a576-b7e8-689b-c6366c1e63d3
title: 'Assignment 3: Fractal Tree Bag'
uid: 5af02bea-0868-c0fa-845e-79cc65770c1e
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---
{{< tableopen >}}{{< tbodyopen >}}{{< tropen >}}{{< tdopen >}}
« Previous: Return to {{% resource_link 65b98bff-a576-b7e8-689b-c6366c1e63d3 "Assignment 3 description" %}}
{{< tdclose >}}{{< tdopen >}}
Next: {{% resource_link 1805af5b-ecab-6b00-7d48-946d9bb9cafe "student work sample" %}} »
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}

*By Elena Jessop, Dawn Wendell and two anonymous MIT students*

{{< resource c36d1cfd-c342-caea-5a24-1f8b81aa48cd >}}

The Fractal Tree Bag

Our concept was to make a canvas bag with a fractal tree design that integrates sensor inputs and LED outputs. The two sensors are (1) a pressure sensor at the bottom of the bag and (2) a touch sensor integrated into the "grass" at the bottom of the tree motif. The outputs are three LEDs.

{{< resource 866bf891-b78a-742c-1a20-ea829fa1db43 >}}

Video of the Fractal Tree Bag in action: dawnw2000. “Fabric PCB Bag.” YouTube. March 3, 2010. Accessed December 2, 2010.

## Circuit Design

{{< resource 21bd5e42-db9c-3d3c-5f00-767e2ed2077c >}}
{{< resource 75cd7d71-ab44-150f-13a2-9ca018c11178 >}}

An initial circuit sketch (left) and circuit diagram (right).

This design was translated into Illustrator and combined with the Tree Motif. The components were then soldered on and encased in epoxy. The soldering was challenging because the conductive fabric would melt if it got too hot. Therefore, some gaps had to be closed with additional wires.

{{< resource d5c884fd-8b49-f308-6dcd-5a879e474943 >}}
{{< resource 008d9dff-1fa9-3e8f-1c94-81ffa5521288 >}}

The finished lasercut pieces before soldering (left), and after soldering and epoxy (right).

{{< resource 0ddf3f85-6d9b-8e5d-8aa6-c26af01a6f73 >}}
{{< resource 9f42838d-dd8c-6143-2ead-38ef8a66460c >}}

Details of soldered and epoxied components.

## Tree Motif Design

The tree motif was chosen because we wanted to integrate fractal patterns into the design. The fractal idea came from this website which talks about polygon fractals.

- McManus, Jerry. "[Polygon Gardens](http://director-online.dasdeck.com/buildArticle.php?id=1119)." Director Online.

The fractal tree was coded in Rhinoscript. The tree was laser cut from 3 separate iron on fabric layers. The first was the conductive fabric, the remaining two were satins.

{{< resource 57a45a7b-0363-cd7f-9e3e-b8ddbc3b88a3 >}}

Tree Motif file, with conductive fabric circuit in blue, and the fractal tree in red.

{{% resource_link ce5f5286-c5f7-8f68-a127-0f979c32ac3b "Large (850x1074) image of the Tree Motif image" %}}

{{< resource 6b750f50-092a-aff8-dc38-bdb76933ce56 >}}

We used a tiny iron to attach the two fabric layers over the conductive layer to avoid melting the epoxy covered surface mounted leds and resistors.

## The Sensors

There are two sensors on the Fractal Tree Bag, the pressure sensor and the touch sensor.

Pressure Sensor

The pressure sensor is a sandwich of conductive fabrics separated by foam and surrounded by felt. This sensor was placed at the bottom of the bag so that it would respond to anything placed in the bag.

{{< resource 43287639-e761-f131-5210-96757e01480d >}}
{{< resource 5cb09dc8-9304-9030-fd11-bf23cf1180ce >}}

The pressure sensor: construction (left) and finished (right).

However, when the pressure sensor was installed in the bottom of the bag, testing showed that the pressure sensor was too sensitive. A layer of neoprene was added with holes cut in it to decrease the sensitivity.

{{< resource 53db2c38-0fcb-d7c6-37ea-5b36ecf48814 >}}
{{< resource 3d719a06-4c46-4f87-7e8c-05cfbb1bc936 >}}

A neoprene layer was added to the pressure sensor to decrease its sensitivity.

## Touch Sensor

The touch sensor is created by sewing conductive and non-conductive threads onto a fabric background. When the sensor is touched, the threads flatten out and make contact, decreasing the resistance across the sensor. The touch sensor was sewn onto the bag to cover the battery holder but the top edge wasn't attached so that the battery can be accessed.

{{< resource b19e89f6-0f76-d196-3cec-ac19c25d61b7 >}}
{{< resource 621221ae-82be-4240-c2a6-7d8db0d70845 >}}
{{< resource b39f8a87-ca94-2fda-2917-0f1065f75765 >}}
{{< resource 0a7885c3-481c-d3b4-0139-edd8662c66e2 >}}

Photos of the Touch Sensor

## The AVR Programming

The code was designed to flash between all the outputs when there were no inputs, and if an input was detected, then only one LED would light up. The code was first tested on one of the pre-made circuits from the in-class demo before being loaded onto the ATtiny13 microcontroller installed on our bag circuit.

Our code ({{% resource_link e675300b-ffcb-e7a3-2a84-880f2c8dba8b "TXT" %}})

## Lessons Learned

- We cut the circuit onto the wrong side of the conductive fabric so the circuit was cut but the paper was not. This was a problem when trying to peel off the paper only in select locations so it could be ironed onto the bag. We solved this problem by taping over the other side of the circuit, peeling off the parts that we didn't want to be ironed, and then ironing over the tape. It worked, but definitely wasn't the ideal case.
- Soldering surface-mount components onto conductive fabric is hard because if the fabric overheats, it burns away. The best technique that we found was to tin the pieces heavily, use lots of flux, and be quick and careful with the soldering iron.
- In attaching our two switch sensors, we originally intended for the switch to close a circuit to ground, and pull the microcontroller pin low. However, we discovered that the open circuit was also read as "low"…most of the time. The floating end of an open circuit was variable, generally reading low but occasionally collecting a voltage value high enough for the microcontroller to read as "high," despite the pin not being pulled to power. We solved this problem by connecting a 10K resistor between the input pin and ground, then attaching one side of the sensor to an input and one side to power. With this arrangement, the pin is pulled to ground when the switch is open. When the switch is closed, the direct connection to power has less resistance than the connection to ground, and so the pin is pulled high.
- Originally we wanted to do the fractal tree (red layer) in leather, we test cut a perfect square of leather at 100power/15speed in the lasercutter. However, our pattern was so delicate that the pieces either burned or did not cut. I think with more time we would find the correct setting to cut these lacy leather kinds of pieces in the lasercutter. Instead we used two silky fabrics to make overlapping layers for the trees these were cut at 50power/50speed

{{< resource 87b04ab2-6cfa-3abf-f18e-8df6b19e221c >}}
{{< resource c7c87f36-84b5-cc37-45e5-e7f5339ce8b8 >}}
{{< resource 17423724-74e2-98f6-24d6-5aea2e16c2e2 >}}
{{< resource be96da9f-275e-0caa-a29d-a2d21e07cd0e >}}

Scenes from the project.

## Contributions

- Elena: AVR Programming, lasercutting
- Anonymous student: design of the conductive paths, design of the tree, lasercutting
- Dawn: initial circuit design, pressure sensor, documentation
- Anonymous student: stroke sensor, artistic elements

{{< tableopen >}}{{< tbodyopen >}}{{< tropen >}}{{< tdopen >}}
« Previous: Return to {{% resource_link 65b98bff-a576-b7e8-689b-c6366c1e63d3 "Assignment 3 description" %}}
{{< tdclose >}}{{< tdopen >}}
Next: {{% resource_link 1805af5b-ecab-6b00-7d48-946d9bb9cafe "student work sample" %}} »
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}