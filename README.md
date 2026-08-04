# Journal of making a keyboard from scratch

## The story

Among all of my microcontroller projects, 90% were made, played with, and forgotten. The only two that stayed with me are a keyboard and a mouse remapper. The office stuff stuck with me the most, and just made me the most satisfied.

In the DIY keyboard community, there are at least 3 groups of people:
- People trying to build the best feeling/looking keyboard
- People trying to build the most ergo keyboard
- People trying to build the most customized keyboard

As a microcontroller hobbyist, I am in the 3rd group. Actually, building keyboards, in the category of microcontroller projects, is one of the easiest projects, considering hardware and firmware solutions are very accessible online. However, for the ultimate customization, I am building things from the ground up.

I made my first fully-customized keyboard 3 years ago. I like most parts of it, but I also learned a lot of lessons:
- 3D printed cases are much less precise than PCB cutouts.
- I never look at the OLED screen, and it is slow to drive.
- Those tiny trackballs feel horrible and are not precise enough to be used as a cursor device.
- Don't use any non-standard key scanning mechanism (I used an I2C extension rather than a diode matrix), which makes things less reliable and slower.
- I should have built the mouse remapper into the keyboard so I could use some key+cursor macros.

In this project, I would like an improvement.

## The Specs

- 60+% layouts
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

## The Process

TODO

## The Show and Tell

TODO