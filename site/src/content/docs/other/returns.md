---
title: 'How do I "fix" my project?'
---

Most projects get returned for the following 3 reasons:

- Missing project files (firmware, step, etc)
- Incomplete CAD 3D model
- Poor quality README
- Bloated/Overkill parts list
- Lack of polish
- Fraud (submitting projects that are not yours)

This doc attempts to quickly explain what each reason means, and how/why you should fix it.

**The goal of the reject/approve system is to help you make real, shipped projects - these are not arbritrary metrics, even if it feels like that sometimes!**

## Missing project files

This means you are missing the source files for your project! It's _really_ important you have these, since it means that other people (hint: this includes reviewers) can actually review your projects

STLs, OBJs, 3MFs, or other mesh formats etc are not valid files for 3D models - they do not preserve

Ideally, post a source file for the respective program (i.e .f3d, .f3d, etc) or a .STEP file.

Make sure you have as much firmware as you can without the physical hardware - almost the entirety of any keyboard's firmware can be generated purely from the schematic, and this also goes for many other projects too.

Please include .kicad_pro, .kicad_sch, and .kicad_pcb files too - gerbers are not enough since it makes your design very hard to modify

## Incomplete 3D model:

This means your CAD model is missing parts that are crucial to your assembly. Just having the case isn't enough - you should also include any electronics (Raspberry Pis, Screens, Motors, etc) that you'll use!

Adding all the electronics & components is really, _really_ important. Not only for yourself, but also because it helps you avoid errors when you're actually assembling your project together.

Unlike software, errors in hardware can be very expensive - not just in money, but also _time_. One wrong part can set you back multiple weeks. You _really_ want to avoid that.

Fortunately, there is a solution to this! Tools like Fusion360 and Onshape allow you to create 1:1 models of your designs vs real life. That means that as long as everything matches up in your 3D model, everything will match in real life too!\*

_granted, this does have some limitations - CAD software has trouble accounting for IRL properties (3D printing inaccuracies, thermal expansion, etc) that need to be accounted for - check out [designing for reality](/design/design-tips/#designing-for-real-life) to learn how to fix this!_

## Poor Quality README:

This one is a pretty easy fix. Usually, it's because you're missing one of the following:

- A description of what the project is and what it does
- A short segment on how you would use the project
- A short segmenet on _why_ you made the project
- Missing images of your project/wiring diagrame/etc.

It's really important you have these because it makes your project understandable - otherwise, whoever is looking at your project is going to spend a _lot_ of time trying to figure the above out!

Do it not just for your reviewer, but also for yourself - it'll help you so much when you look back on this project in 2-3 years and have forgotten the details.

## Overpriced Bill Of Materials (BOM)

This is usually a rejection because you're asking to get parts that are way more powerful than what you need, or cost a disproportionate amount relative to your design difficulty.

A very common example is getting $300 custom CNC'd parts, super high quality ESCs, etc. for a simple battlebot or drone. While it would be awesome to be able to give funding for projects like these, the problem is that the majority of the cost goes into parts that you had almost 0 hand in designing.

If, for example, you instead designed your own ESCs, transmitters, etc, $300 would be totally reasonable to give! This is because the majority of the cost goes into a component that you yourself designed.

Another example is getting extra parts / things that are just not needed:

- An entire spool of filament for a 100g print
- An extra MCU "just in case"
- ENIG PCBs

The last example is just poor part sourcing. This means getting an arduino for $35, a stepper motor for $20, etc. This usualy just means you need to buy from better suppliers! This one's an easy fix, check out the sourcing guide at highway.hackclub.com

It's really important that we are all efficient with our projects, because it means every bit of money we have can go further in the program.

_this is the judgement that has the most wiggle room - if you feel like you should have an exception, please ask an organizer in your program!_

## Lack of polish

_what the heck is project polish?_

Polishing your project is the process of turning your project from a minimum technical demo to a completed project.

The easiest way to think of polishing your design is adding detail to it!

For example, on a functional level, almost every keyboard can be reduced down to a 60%/75%/TKL layout in a flat rectangular block

What makes them cool & unique are all the details that the designers put in - the different tilt angles, chamfers, engravings, etc.

Let's take a look at orpheuspad, the example macropad I made for hackpad - it's not a keyboard, but the same principles apply.

Here's what it looked like as a purely functional prototype:

<img src="https://cdn.hackclub.com/rescue?url=https://hc-cdn.hel1.your-objectstorage.com/s/v3/600c5d170ef8341a36e90ad14c53245d383afd15_image.png" width="400"/>

Looks decent, but could be _way_ better. Here's what it looks like after I polished it a ton!

<img src="https://cdn.hackclub.com/rescue?url=https://hc-cdn.hel1.your-objectstorage.com/s/v3/a00982621f8f94532ac8d508a83f39504c0a2b4c_image.png" width="400"/>

Notice the details? I added the following:

- Embossed riangle pattern in the middle
- 5 degree tilt at the bottom
- Rounded corners
- Chamfers across the entire case
- Embossed Hack Club "h" logo in the top right
- First layer colour change
- Different heights on the acrylic

There's more, but what I want you to notice is how _none_ of those changes are functional, yet they made the project way better & cooler. I turned orpheuspad from a plain rectangular block, to a sharp, tech-themed desk gadget.

This is what we mean when we ask for project polish. It's the process of turning your demo into a finished project.

A very important thing to remember is that making hardware projects is usually more than a pure engineering challenge - it's also in many respects an artistic endeavour.

<!-- (need help making it look good? check out the guide here) -->

## Fraud

The following is classified as design fraud:

- Following tutorials almost exactly 1:1
- Submitting projects designed by other people as your own

Any convicted fraud will result in a permanent ban from hardware programs. _do not commit fraud_
