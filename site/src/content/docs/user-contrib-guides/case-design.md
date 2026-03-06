---
title: "Designing PCB cases"
---

Written by: [Person20020/Koji](https://hackclub.enterprise.slack.com/team/U07QNKS5SKA)

Designing a nice case for your PCB projects can be the thing that takes it from something that looks like a cool idea to a well polished project that is ready to ship.

I use KiCad and FreeCAD but other software will be pretty similar. I won't be saying exactly what buttons to press but rather the process to go through.


## Prepare Your PCB
The most helpful thing that I have found is having a good model of your PCB to design around. Many footprints in KiCad already have a model but for custom footprints that you have imported or those that are less common you may need to add your own.

Probably the best resource for models like this is the [Grabcad library](https://grabcad.com/library). It has a ton of detailed models of all sorts of parts. It is user contributed though so you should check dimensions with the datasheet. 
If you can't find a good model online, you can also look at the datasheet and model them yourself.

Once you have your models, go through each footprint and assign it. Tiny parts like SMD resistors or capacitors are fine to ignore but anything that is large enough to impact the design of the case should ideally have a model. (Make sure to include stuff like connectors and buttons where the positions will be important in your design.)

![PCB with components](/user-contrib-guides-media/case-design/PCB-with-components.png)

You can then export your PCB. Make sure that you include the board body and the components. If your PC is isn't very powerful you can exclude all of the conductors and silkscreen to keep the model simple.


## Design the Case
First import the PCB into your CAD program. In FreeCAD you can drag and drop the step file but in Fusion 360 you can use `File -> Upload`. In Fusion this will import the step file as a bunch of individual parts so it can be helpful to do the following to put it inside of a component:

1. Create a new file
2. Create a component and save the file (Make sure the component is activated. It should have a dot next to it like this.)
![activated component](/user-contrib-guides-media/case-design/create-component.png)
3. Go back to the first file
    - Select everything
    - Click `Create -> Derive`
    - Set destination to 'Existing Design'
    - Click 'OK' and select the other file you created

This will put everything in the component in the new file.

Once you have the PCB you can start on the case. For simple projects where the case is just an enclosure for the PCB (maybe some buttons, a display, connectors, or things like that) it can be easiest to start by making a simple box shape and then add detail after. 

This was my process:
1. Start with a basic shape enclosing the whole PCB
![Basic enclosure](/user-contrib-guides-media/case-design/basic-case-design-1.png)
2. Make important features like cutouts for connectors and the push button
![Add cutouts and important features](/user-contrib-guides-media/case-design/basic-case-design-2.png)
3. Clean up the features - Add cutouts for clearance, fillets, chamfers, etc.
![Clean up features](/user-contrib-guides-media/case-design/basic-case-design-3.png)
4. Add mounting - Add printed standoffs (or something else) to hold the PCB in place and screw holes to keep the case closed.
![Add mounting](/user-contrib-guides-media/case-design/basic-case-design-4.png)

<video controls>
    <source src="https://cdn.hackclub.com/019cbf8f-cf88-7dc4-b9b4-ce7e01afa3e2/Case%20Design%20Guide-Basic%20Case.mp4" type="video/mp4">
</video>

> <small>An example video of designing a case for a USB hub at 8x speed. I forgot to add a hole for the port on the back but it is the exact same process.</small>

For mounting there are a few ways of doing things. In this example I used printed standoffs built into the case with an undersized hole to screw an m2 screw directly into. 

These are some methods you can try:
- Threading screws into printed standoffs
- Heat set inserts or metal standoffs if you need it to be more durable
- Plain old nuts/bolts
- Printed clips/brackets/mechanisms (if done well these can be really nice and make it easy to work with)
- Hot glue for non mechanical parts (stuff that just needs to be stuck somewhere to stop it from moving). It is still usually good to have a recess or something to help position things well.

The mounting method you choose will depend a lot on the constraints of your design. (e.g. do you care about screw holes? do you have space for heat set inserts?)


## Decoration / Art / Polish
At this point you have a case that is fully functional and could be used as is, but there is still a lot you can do to make it a 'polished' project.

[This](/other/returns/#lack-of-polish) explains pretty well what polish is but basically it is all of the details that you can add to get it from a basic functioning project to something that looks original and 'complete'.

The orpheuspad is a great example of a polished project. All the edges are rounded/chamfered, it has accent colors, a logo, and in general looks like a finished project.

![orpheuspad](https://cdn.hackclub.com/rescue?url=https://hc-cdn.hel1.your-objectstorage.com/s/v3/a00982621f8f94532ac8d508a83f39504c0a2b4c_image.png)
