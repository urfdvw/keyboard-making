# Journal of making a keyboard from scratch

## The story

Among all of my microcontroller projects, 90% were made, played with, and forgotten. The only two that stayed with me are a keyboard and a mouse remapper. The office stuff stuck with me the most, and just made me the most satisfied.

In the DIY keyboard community, there are at least 3 groups of people:
- People trying to build the best feeling/looking keyboard
- People trying to build the most ergo keyboard
- People trying to build the most customized keyboard

As a microcontroller hobbyist, I am in the 3rd group. Actually, building keyboards, in the category of microcontroller projects, sounds like one of the easiest projects: it's just a set of buttons. What could go wrong?

So I designed and made my first keyboard 3 years ago from the ground up. I like most parts of the outcome, but it turned out to be a fairly complex project, balancing standard parts, customization, aesthetics, and cost.

During the project I learned a lot of lessons:
- 3D printed cases are much less precise than PCB cutouts.
- I never look at the OLED screen, and it is slow to drive.
- Those tiny trackballs feel horrible and are not precise enough to be used as a cursor device.
- Don't use any non-standard key scanning mechanism (I used an I2C extension rather than a diode matrix), which makes things less reliable and slower.
- I should have built the mouse remapper into the keyboard so I could use some key+cursor macros.

## The Specs

I am making two builds. They are identical in everything below except the layout.

- two 60+% layouts
    - one customized typewriter
    - one ortholinear
- reverse slope for ergo gesture
- with regular keycap and stabilizer sizes (for lower cost)
- use PCB for the circuit, plate, and also the case. Yeah, I'm just checking it out to see if it makes sense.
- touchpad/hand rest built in, with haptic feedback
- built-in USB host for a mouse, for cursor remapping
- touch button on the left panel serving as the ESC button
- no RGB, no screen
- diode grid, as normal keyboards do
- CircuitPython firmware, written by me
- Macro pad function built in

## The Process

### Layout design

Layout design needs to be done before anything else, because I need to visualize the proposed layout and prove it practical (mostly by thought experiment). Also, the following steps will rely on this design decision.

[keyboard-layout-editor.com](https://www.keyboard-layout-editor.com/) is a perfect tool for this. I can edit in a WYSIWYG UI, but my favorite method is to directly edit the raw text.

I have two designs I want to try out. The first design is a normal-looking but slightly customized layout, which I call the typewriter. This is an improved version of my previous build.

![typewriter](./layouts/typewriter.png)

The ideas are:
- regular typewriter layout for the first 4 rows
- four modifier keys on the left, resembling a Mac
- the Mn (Macro layer) and M1~M4 (macro keys) are at the positions of the trackball and OLED in the last version.
- ESC is not on the layout because it will be on the side panel as a touch button

In the second build, I want to challenge myself to try some other layouts. I am not a huge fan of those crazy ergo layouts because the learning cost is too high. However, I am very convinced by ortholinear.

![ortholinear](./layouts/ortholinear.png)

The ideas are similar to the ones above:
- using a regular keycap set, but arranged in an ortholinear layout
- there is space for ESC, so why not add it back
    - note that the touch button is still there, so I can use it as a macro button
- no space for macro keys, but the macro layer key can be there.

The raw text of the two layouts is in the ./layouts/ folder.

## The Show and Tell

TODO