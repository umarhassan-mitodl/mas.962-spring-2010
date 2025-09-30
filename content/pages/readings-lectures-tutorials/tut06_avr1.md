---
content_type: page
description: ''
draft: false
hide_download: true
hide_download_original: null
learning_resource_types: []
ocw_type: CourseSection
parent_title: Readings, Lectures & Tutorials
parent_type: CourseSection
parent_uid: e974bd1a-9897-6b46-896a-13de54082f58
title: 'AVR Programming Tutorial, Part 1: Downloading Programs'
uid: 4bbdee6e-bb42-6142-21cf-13f92a364c47
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---
« {{% resource_link b8152aef-691c-0825-0ce2-97f34c7b6768 "Laser Cutter Tutorial" %}} | {{% resource_link e974bd1a-9897-6b46-896a-13de54082f58 "Readings, Lectures & Tutorials Index" "#ses6" %}} | {{% resource_link a860002e-582c-fa35-4e45-5b5e787595e0 "AVR Programming, Part 2" %}} »

**1\. Make sure you've installed the necessary software.**

Mac: [CrossPack](http://www.obdev.at/products/crosspack/index.html)

Windows: [WinAVR](http://winavr.sourceforge.net/index.html)

Important Note for people running Windows: on Windows you will also have to install the driver for the USB programmer. If the driver does not successfully install automatically after you plug in the programmer, try downloading the latest libusb driver from [SourceForge](http://sourceforge.net/projects/libusb-win32/files/libusb-win32-releases/).

Unfortunately Windows 7 does not support the USB programmer we will be using, so if you have a machine with Windows 7 you should use the Mac computer in the high-low tech lab to do your programming.

For windows Vista 64, you need to first install AVR Studio 4. then install WinAVR 20100110. Then, download msys-1.0-vista64.zip ([ZIP](https://courses.media.mit.edu/2010spring/mas962/2010/uploads/Main/msys-1.0-vista.zip)) and put that into your winavr/utils/bin directory. Then things should compile.

**2\. Get your materials together**

[ATtiny13](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail&name=ATTINY13V-10PU-ND) on a fabric PCB

[AVRISP programmer](http://search.digikey.com/scripts/DkSearch/dksus.dll?Cat=2621880&k=avrisp) with homemade alligator clip attachment

USB cable

**3\. Download some code**

Download and unzip NewTextilesAVR.zip ([ZIP](https://courses.media.mit.edu/2010spring/mas962/2010/uploads/Main/NewTextilesAVR.zip)) which contains all of the files you'll need. Put the NewTextilesAVR folder on your desktop.

**4\. Open up a terminal window, a window that allows you to type out commands to send to your computer**

On a Mac, go to the Applications→Utilities folder and open Terminal.app.

On a PC, go the Start menu and select Run. Then type cmd in the text box that pops up.

**5\. Navigate to the code folder within the NewTextilesAVR folder or "directory"**

On a Mac, type the following command: `cd Desktop/NewTextilesAVR/code`

The cd stands for "change directory".

**6\. Plug in your programmer and attach your circuit to your computer**

Here is the pin layout diagram for the ATtiny13 chip – the miniature computer that we'll be using. The diagram is from the ATtiny13 datasheet ([PDF - 2.9MB](http://www.atmel.com/dyn/resources/prod_documents/doc2535.pdf)).

{{< resource 6234ff23-46d3-ac37-1ce6-9d856ba8f1a2 >}}

ATiny13 pinout diagram. (© Atmel. All rights reserved. This content is excluded from our Creative Commons license. For more information, see [http://ocw.mit.edu/fairuse](/fairuse))

The first important thing to know is how to orient the chip to the diagram. We need to know which way is up. If you look closely at the chip you will see a small dot in one corner. This dot indicates the top of the chip. When you match your chip to the diagram, the dot should be in the upper left hand corner of the chip, like so:

{{< resource 4b62a501-2cab-1cf8-07e3-f2953f14ec42 >}}

Orienting your ATiny13 device.

The diagram also shows the different functions of each leg of the ATtiny13 chip. To program the chip–to tell it what to do–we need to attach certain legs to our programmer.

Clip the programmer to your circuit, attaching the labeled alligator clips to the appropriate legs of the chip. Refer to the diagram above and follow the traces of your circuit. We need to attach + (also called "VCC" or "power" and usually colored red), - (also called "GND" or "ground" and usually colored black), RESET, MOSI, MISO, and SCK. Use the round piece of plexiglass to support your circuit. Here is a photograph that shows what the physical attachment should look like.

{{< resource bbd2e820-7e9b-5119-6e4a-15335494bbc6 >}}

Attaching programmer to the ATiny13 using your circuit.

NOTE: IF YOUR CHIP IS GETTING HOT AFTER YOU ATTACH IT, UNPLUG EVERYTHING IMMEDIATELY. THIS MEANS YOU HAVE A SHORT & YOU'RE FRYING YOUR CHIP & MAYBE THE PROGRAMMER TOO.

**7\. Program your chip.**

Type the following command in Terminal: `make clean && make && make install`

If all goes well, the LED on your fabric circuit should begin to blink.

**8\. Open the blink.c program file.**

Browse to the NewTextilesAVR directory, open the code folder and double click the blink.c file to open it in a text editor.

Now we're ready to start writing our own program… see {{% resource_link a860002e-582c-fa35-4e45-5b5e787595e0 "AVR Programming Tutorial, Part 2: Writing Programs" %}}.

« {{% resource_link b8152aef-691c-0825-0ce2-97f34c7b6768 "Laser Cutter Tutorial" %}} | {{% resource_link e974bd1a-9897-6b46-896a-13de54082f58 "Readings, Lectures & Tutorials Index" "#ses6" %}} | {{% resource_link a860002e-582c-fa35-4e45-5b5e787595e0 "AVR Programming, Part 2" %}} »